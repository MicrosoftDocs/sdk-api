---
UID: NF:winuser.GetPointerType
title: GetPointerType function
author: windows-sdk-content
description: Retrieves the pointer type for a specified pointer.
old-location: inputmsg\getpointertype.htm
old-project: InputMsg
ms.assetid: 63bfc340-9691-463c-96ca-0a5b80b8fe40
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetPointerType, GetPointerType function [Input Messages and Notifications], inputmsg.getpointertype, winuser/GetPointerType
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
 - GetPointerType
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPointerType function


## -description


Retrieves the pointer type for a specified pointer.


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve pointer type.


### -param pointerType [out]

An address of a <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">POINTER_INPUT_TYPE</a> type to receive a pointer input type.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



An application can use the <b>GetPointerType</b> function to determine the pointer type if it wishes to react differently to pointers of different types.

<div class="alert"><b>Note</b>  This function will never return with the generic <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_POINTER </a>type.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

