---
UID: NF:winuser.GetPointerInfo
title: GetPointerInfo function
author: windows-sdk-content
description: Gets the information for the specified pointer associated with the current message.
old-location: inputmsg\getpointerinfo.htm
old-project: InputMsg
ms.assetid: 75faea24-91cd-448b-b67a-19fe530f1800
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPointerInfo, GetPointerInfo function [Input Messages and Notifications], inputmsg.getpointerinfo, winuser/GetPointerInfo
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
 - GetPointerInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPointerInfo function


## -description


Gets the information for the specified pointer associated with the current message.
<div class="alert"><b>Note</b>  Use <a href="https://msdn.microsoft.com/63bfc340-9691-463c-96ca-0a5b80b8fe40">GetPointerType</a> if you don't need the additional information exposed by <b>GetPointerInfo</b>.</div><div> </div>

## -parameters




### -param pointerId [in]

The pointer identifier.


### -param pointerInfo [out]

Address of a  <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> structure that receives the pointer information.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetPointerInfo</b> retrieves information for a single pointer associated with a pointer message. 

Use <a href="https://msdn.microsoft.com/6b7f450d-6ab1-4991-b2f9-a1db3f065711">GetPointerFrameInfo</a> to retrieve frame information associated with a message  for a set of pointers.

The information returned by <b>GetPointerInfo</b> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.

If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac222">WM_POINTERUPDATE</a> message. Use <a href="https://msdn.microsoft.com/92173197-45e8-4ee7-8959-2f14f90c2d21">GetPointerInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. Note that this may be the window to which the input was originally delivered or it may be a window to which the message was forwarded.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/6b7f450d-6ab1-4991-b2f9-a1db3f065711">GetPointerFrameInfo</a>



<a href="https://msdn.microsoft.com/1ae035d6-a375-4421-82a6-50be4a2341f6">GetPointerFrameInfoHistory</a>



<a href="https://msdn.microsoft.com/92173197-45e8-4ee7-8959-2f14f90c2d21">GetPointerInfoHistory</a>
 

 

