title: Hello World
---
Welcome to [vincent.byfinal.com](http://vincent.byfinal.com/)! 

## Code Time

```
    public static String makeOutputString(Map<String, Object> map, long offset) {
        if (map == null || map.isEmpty()) {
            return "";
        }

        StringBuilder sb = new StringBuilder();
        int count = 0;
        for (Map.Entry<String, Object> entry : map.entrySet()) {
            String key = entry.getKey();
            String value = (String) entry.getValue();
            if (Strings.isNullOrEmpty(key)) {
                continue;
            }
            if (count != 0) {
                sb.append("&");
            }
            sb.append(key).append("=").append(value);
            count++;
        }
        sb.append("&inputOffset=").append(offset);

        return sb.toString();
    }
```
