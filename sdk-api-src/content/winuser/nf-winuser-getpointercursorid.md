---
UID: NF:winuser.GetPointerCursorId
title: GetPointerCursorId function
author: windows-sdk-content
description: Retrieves the cursor identifier associated with the specified pointer.
old-location: inputmsg\getpointercursorid.htm
tech.root: InputMsg
ms.assetid: 43211600-ee82-416f-860f-423c581eda75
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPointerCursorId, GetPointerCursorId function [Input Messages and Notifications], inputmsg.getpointercursorid, winuser/GetPointerCursorId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-WMPointer-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerCursorId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPointerCursorId function


## -description


Retrieves the cursor identifier associated with the specified pointer.


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve the cursor identifier.


### -param cursorId [out]

An address of a <b>UINT32</b> to receive the tablet cursor identifier, if any, associated with the specified pointer.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Cursor objects represent pointing and selecting devices used with digitizer devices, most commonly tactile contacts on touch digitizers and tablet pens on pen digitizers. Physical pens may have multiple tips (such as normal and eraser ends), with each pen tip representing a different cursor object. Each cursor object has an associated cursor identifier.

For pointer types that derive from these cursor objects, an application can use the <b>GetPointerCursorId</b> function to retrieve the cursor identifier associated with a pointer.






## -see-also




<a href="https://msdn.microsoft.com/0123DCD0-DAE1-4AC2-AB36-23D114803138">Functions</a>
 

 

