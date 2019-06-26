---
UID: NF:winbase.SetHandleCount
title: SetHandleCount
ms.date: 4/26/2019
ms.keywords: SetHandleCount
ms.topic: language-reference
f1_keywords:
 - "winbase/SetHandleCount"
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: winbase.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
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
 - kernel32.dll
api_name:
 - SetHandleCount
---

## -description

Changes the number of file handles available to a process.  For DOS-based Win32, the default maximum number of file handles available to a process is 20.  For Windows Win32 systems, this API has no effect.

## -parameters

### -param uNumber

The requested number of available file handles.

## -returns

The number of available file handles. 

## -remarks

## -see-also
f1_keywords: 
 - "winbase/SetFirmwareEnvironmentVariable"
