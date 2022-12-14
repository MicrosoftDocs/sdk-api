---
UID: NF:oleidl.HDC_UserSize
tech.root: com
title: HDC_UserSize (oleidl.h)
ms.date: 08/15/2022
targetos: Windows
description: The HDC_UserSize function (oleidl.h) calculates the wire size of the HDC object and gets its handle and data.
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
 - ole32.dll
api_name:
 - HDC_UserSize
f1_keywords:
 - HDC_UserSize
 - oleidl/HDC_UserSize
dev_langs:
 - c++
helpviewer_keywords:
 - HDC_UserSize
---

## -description

Calculates the wire size of the HDC object and gets its handle and data.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the HDC object to be properly aligned when it will be marshaled to the buffer.

### -param unnamedParam3 [in]

The object.

## -returns

## -remarks

## -see-also

