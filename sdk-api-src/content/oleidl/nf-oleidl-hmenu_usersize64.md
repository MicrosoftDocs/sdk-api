---
UID: NF:oleidl.HMENU_UserSize64
tech.root: com
title: HMENU_UserSize64 (oleidl.h)
ms.date: 08/15/2022
targetos: Windows
description: The HMENU_UserSize64 function (oleidl.h) calculates the wire size of the HMENU object and gets its handle and data.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: oleidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-marshal-l1-1-0.dll
 - ole32.dll
api_name:
 - HMENU_UserSize64
f1_keywords:
 - HMENU_UserSize64
 - oleidl/HMENU_UserSize64
dev_langs:
 - c++
helpviewer_keywords:
 - HMENU_UserSize64
---

## -description

Calculates the wire size of the HMENU object and gets its handle and data.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the HMENU object to be properly aligned when it will be marshaled to the buffer.

### -param unnamedParam3 [in]

The object.

## -returns

## -remarks

## -see-also

