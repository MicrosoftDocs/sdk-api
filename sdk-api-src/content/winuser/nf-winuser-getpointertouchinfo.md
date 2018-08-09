---
UID: NF:winuser.GetPointerTouchInfo
title: GetPointerTouchInfo function
author: windows-sdk-content
description: Gets the touch-based information for the specified pointer (of type PT_TOUCH) associated with the current message.
old-location: inputmsg\getpointertouchinfo.htm
old-project: InputMsg
ms.assetid: 97d93754-fc7e-4400-a6ee-6bab53e421cf
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPointerTouchInfo, GetPointerTouchInfo function [Input Messages and Notifications], inputmsg.getpointertouchinfo, winuser/GetPointerTouchInfo
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
 - GetPointerTouchInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPointerTouchInfo function


## -description


Gets the touch-based information for the specified pointer (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>) associated with the current message. 


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve information.


### -param touchInfo [out]

Address of a <a href="https://msdn.microsoft.com/fee176ba-ad07-3141-ab4d-1b8c335fd102">POINTER_TOUCH_INFO</a> structure to receive the touch-specific pointer information.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetPointerTouchInfo</b> retrieves information for a single pointer (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>) associated with a pointer message. 

Use <a href="https://msdn.microsoft.com/a100cc7a-62fc-4ace-8d35-e77aff98d944">GetPointerFrameTouchInfo</a> to retrieve frame information associated with a message  for a set of pointers.

The information returned by <b>GetPointerTouchInfo</b> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.

If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac222">WM_POINTERUPDATE</a> message. Use <a href="https://msdn.microsoft.com/9fdfbde7-4126-4c1b-b870-479f846e1aa9">GetPointerTouchInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. Note that this may be the window to which the input was originally delivered or it may be a window to which the message was forwarded.

If the specified pointer is not of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/a100cc7a-62fc-4ace-8d35-e77aff98d944">GetPointerFrameTouchInfo</a>



<a href="https://msdn.microsoft.com/f2521a67-9850-46e9-bc8b-75bf5b6cc263">GetPointerFrameTouchInfoHistory</a>



<a href="https://msdn.microsoft.com/9fdfbde7-4126-4c1b-b870-479f846e1aa9">GetPointerTouchInfoHistory</a>
 

 

