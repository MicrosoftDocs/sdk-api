---
UID: NF:webservices.WsCountOf
title: WsCountOf macro (webservices.h)
description: Returns the number of elements a specified array.
helpviewer_keywords: ["WsCountOf","WsCountOf macro [Web Services for Windows]","webservices/WsCountOf","wsw.wscountof"]
old-location: wsw\wscountof.htm
tech.root: wsw
ms.assetid: 3087fa5e-46fc-4580-999c-f80a2b8555f6
ms.date: 07/01/2025
ms.keywords: WsCountOf, WsCountOf macro [Web Services for Windows], webservices/WsCountOf, wsw.wscountof
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsCountOf
 - webservices/WsCountOf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WsCountOf
---

# WsCountOf macro

## -syntax

```cpp
ULONG WsCountOf(
  [in]   arrayValue
);
```

## -returns

Type: **ULONG**

The number of elements in the array.


## -description

Returns the number of elements a specified array.

## -parameters

### -param arrayValue [in]

The array of objects  for which for which to get the count.
        The array type can be either a valid C data type or user defined data type. The array must be static.

