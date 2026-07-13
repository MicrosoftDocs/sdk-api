---
UID: NF:winbase.SetHandleCount
title: SetHandleCount
description: The SetHandleCount function changes the number of file handles available to a process.
ms.date: 08/04/2022
ms.keywords: SetHandleCount
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: winbase.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - SetHandleCount
 - winbase/SetHandleCount
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-kernel32-l2-1-0.dll
 - api-ms-win-core-misc-l1-1-0.dll
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - api-ms-win-core-kernel32-legacy-l1-1-5.dll
 - api-ms-win-core-kernel32-legacy-l1-1-4.dll
 - api-ms-win-core-kernel32-legacy-l1-1-3.dll
 - api-ms-win-core-kernel32-legacy-l1-1-2.dll
 - api-ms-win-core-kernel32-legacy-l1-1-1.dll
 - api-ms-win-core-kernel32-legacy-l1-1-0.dll
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

