# lua-5.3.5-shadow-warnings
Lua 5.3.5 with compiler warnings for shadowed variables

Example:
```
local xv = 34
for xv=1,5 do print(xv) end
function doIt(v)
    local v = v or 33
    print(v)
end
doIt(44)
```
Output:
```
src/lua test.lua 
test.lua:2: warning Name [xv] already declared will be shadowed
test.lua:4: warning Name [v] already declared will be shadowed
1
2
3
4
5
44

```
