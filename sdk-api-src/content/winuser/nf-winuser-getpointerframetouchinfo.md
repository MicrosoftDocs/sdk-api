---
UID: NF:winuser.GetPointerFrameTouchInfo
title: GetPointerFrameTouchInfo function
author: windows-sdk-content
description: Gets the entire frame of touch-based information for the specified pointers (of type PT_TOUCH) associated with the current message.
old-location: inputmsg\getpointerframetouchinfo.htm
tech.root: InputMsg
ms.assetid: a100cc7a-62fc-4ace-8d35-e77aff98d944
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPointerFrameTouchInfo, GetPointerFrameTouchInfo function [Input Messages and Notifications], inputmsg.getpointerframetouchinfo, winuser/GetPointerFrameTouchInfo
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
 - GetPointerFrameTouchInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPointerFrameTouchInfo function


## -description


Gets the entire frame of touch-based information for the specified pointers (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>) associated with the current message. 


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve frame information.


### -param pointerCount [in, out]

A pointer to a variable that specifies the count of structures in the buffer to which touchInfo points. If <b>GetPointerFrameTouchInfo</b> succeeds, <i>pointerCount</i> is updated with the total count of pointers in the frame.


### -param touchInfo [out]

Address of an array of <a href="https://msdn.microsoft.com/fee176ba-ad07-3141-ab4d-1b8c335fd102">POINTER_TOUCH_INFO</a> structures to receive the pointer information. This parameter can be NULL if <i>*pointerCount</i> is zero.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Parallel-mode devices may report pointer input in frames, that is, they may report the state and position of all pointers from that device in a single input report to the system. Ideally, applications should view the entire frame as a single input unless the application-specific requirements dictate otherwise.

<b>GetPointerFrameTouchInfo</b> retrieves the entire pointer input frame associated with a pointer (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>) message. Use <a href="https://msdn.microsoft.com/97d93754-fc7e-4400-a6ee-6bab53e421cf">GetPointerTouchInfo</a> to retrieve information for a single pointer associated with a pointer message.

The  frame contains only pointers that are currently owned by the same window as the specified pointer.

The information returned by <b>GetPointerFrameTouchInfo</b> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.



If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac222">WM_POINTERUPDATE</a> message. Use <a href="https://msdn.microsoft.com/f2521a67-9850-46e9-bc8b-75bf5b6cc263">GetPointerFrameTouchInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

Having retrieved the entire frame of information, the application can then call the <a href="https://msdn.microsoft.com/d67f8d44-3e19-4523-a0f3-38f09f5df91f">SkipPointerFrameMessages</a> function to skip remaining pointer messages associated with this frame that are pending retrieval. This saves the application the overhead of retrieving and processing the remaining messages one by one. However, the <b>SkipPointerFrameMessages</b> function should be used with care and only when the caller can be sure that no other entity on the caller’s thread is expecting to see the remaining pointer messages one by one as they are retrieved.

Note that the information retrieved is associated with the pointer frame most recently retrieved by the calling thread. Once the calling thread retrieves its next message, the information associated with the previous pointer frame may no longer be available.

If the pointer frame contains no additional pointers besides the specified pointer, this function succeeds and returns only the information for the specified pointer.

If the information associated with the pointer frame is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified pointer is not of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.



For apps that have  both client and non-client areas, the input frame can include both client and non-client data. To differentiate between client and non-client data, you must perform hit testing on the target window.

We recommend the following if you want to filter data from the input frame:

<ul>
<li>For each update that does not include a pointer contact (a <a href="https://msdn.microsoft.com/CC3F8E21-F4FF-495C-922E-A3708D3F2093">POINTER_FLAG_UPDATE</a> without <b>POINTER_FLAG_INCONTACT</b>), hit test to determine if the input is client or non-client.</li>
<li>For each new contact (<a href="https://msdn.microsoft.com/CC3F8E21-F4FF-495C-922E-A3708D3F2093">POINTER_FLAG_DOWN</a>), hit test to determine if the input is client or non-client and track this info.</li>
<li>For each update that includes a pointer contact (a <a href="https://msdn.microsoft.com/CC3F8E21-F4FF-495C-922E-A3708D3F2093">POINTER_FLAG_UPDATE</a> with <b>POINTER_FLAG_INCONTACT</b>), use the tracking info to determine whether the input is client or non-client.</li>
<li>For each <a href="https://msdn.microsoft.com/CC3F8E21-F4FF-495C-922E-A3708D3F2093">POINTER_FLAG_UP</a>, use the tracking info to determine whether the input is client or non-client and then clear this pointer from the tracking data.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/0123DCD0-DAE1-4AC2-AB36-23D114803138">Functions</a>



<a href="https://msdn.microsoft.com/f2521a67-9850-46e9-bc8b-75bf5b6cc263">GetPointerFrameTouchInfoHistory</a>



<a href="https://msdn.microsoft.com/97d93754-fc7e-4400-a6ee-6bab53e421cf">GetPointerTouchInfo</a>



<a href="https://msdn.microsoft.com/9fdfbde7-4126-4c1b-b870-479f846e1aa9">GetPointerTouchInfoHistory</a>
 

 

