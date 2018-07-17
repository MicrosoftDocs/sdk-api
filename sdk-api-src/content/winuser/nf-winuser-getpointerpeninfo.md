---
UID: NF:winuser.GetPointerPenInfo
title: GetPointerPenInfo function
author: windows-sdk-content
description: Gets the pen-based information for the specified pointer (of type PT_PEN) associated with the current message.
old-location: inputmsg\getpointerpeninfo.htm
old-project: InputMsg
ms.assetid: 5f1f7252-a4aa-4b06-94c9-2aa365cf0100
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: GetPointerPenInfo, GetPointerPenInfo function [Input Messages and Notifications], inputmsg.getpointerpeninfo, winuser/GetPointerPenInfo
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
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerPenInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPointerPenInfo function


## -description


Gets the pen-based information for the specified pointer (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a>) associated with the current message. 


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve information.


### -param penInfo [out]

Address of a <a href="https://msdn.microsoft.com/fee176ba-ad07-4141-ab4d-1b8c335fd111">POINTER_PEN_INFO</a> structure to receive the pen-specific pointer information.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetPointerPenInfo</b> retrieves information for a single pointer (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a>) associated with a pointer message. 

Use <a href="https://msdn.microsoft.com/52db9b96-7f9e-41d7-88f7-b9c7691a6511">GetPointerFramePenInfo</a> to retrieve frame information associated with a message  for a set of pointers.

The information returned by <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-19fe530f1800">GetPointerInfo</a> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.

If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac222">WM_POINTERUPDATE</a> message. Use <a href="https://msdn.microsoft.com/90082327-b242-4f5d-8cd7-fd8ef9340395">GetPointerPenInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. Note that this may be the window to which the input was originally delivered or it may be a window to which the message was forwarded.

If the specified pointer is not of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/52db9b96-7f9e-41d7-88f7-b9c7691a6511">GetPointerFramePenInfo</a>



<a href="https://msdn.microsoft.com/a4f6a9f3-dfbd-4413-aae7-f58e1521ef1d">GetPointerFramePenInfoHistory</a>



<a href="https://msdn.microsoft.com/90082327-b242-4f5d-8cd7-fd8ef9340395">GetPointerPenInfoHistory</a>
 

 

