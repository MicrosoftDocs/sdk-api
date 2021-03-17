---
UID: NS:ws2spi.WSPData
title: WSPDATA
description: The WSPDATA structure contains service provider information.
tech.root: winsock
helpviewer_keywords: ["WSPData","WSPDATA"]
ms.date: 4/26/2019
ms.keywords: WSPData, WSPDATA
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.typenames: WSPDATA, *LPWSPDATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ws2spi.h
api_name:
 - WSPData
 - WSPDATA
f1_keywords:
 - WSPData
 - ws2spi/WSPData
 - LPWSPDATA
 - ws2spi/LPWSPDATA
 - WSPDATA
 - ws2spi/WSPDATA
---

## -description

The **WSPDATA** structure contains service provider information.

## -struct-fields

```C++
} WSPDATA, *LPWSPDATA;
```

### -field wVersion

Version of the Windows Sockets SPI specification that the Windows Sockets service provider expects the caller to use.

### -field wHighVersion

Highest version of the Windows Sockets SPI specification that this service provider can support (also encoded as above). Normally this will be the same as **wVersion**.

### -field szDescription

Null-terminated Unicode string into which the Windows Sockets provider copies a description of itself. The text (up to 256 characters in length) can contain any characters except control and formatting characters: the most likely use to which an SPI client will put this is to display it (possibly truncated) in a status message.

## -remarks

## -see-also

<b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a></b>

