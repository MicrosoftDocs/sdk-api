---
UID: NF:winuser.GetPointerInputTransform
title: GetPointerInputTransform function
author: windows-sdk-content
description: Gets one or more transforms for the pointer information coordinates associated with the current message.
old-location: inputmsg\getpointerinputtransform.htm
old-project: InputMsg
ms.assetid: 9F10ED61-90E3-441B-8F4D-E33DA54D473C
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPointerInputTransform, GetPointerInputTransform function [Input Messages and Notifications], inputmsg.getpointerinputtransform, winuser/GetPointerInputTransform
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
 - GetPointerInputTransform
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPointerInputTransform function


## -description


Gets one or more transforms for the pointer information coordinates associated with the current message.



## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve information.


### -param historyCount [in]

The number of <a href="https://msdn.microsoft.com/DE6854F0-17D8-4E4B-97CB-A135910A300C">INPUT_TRANSFORM</a> structures that <i>inputTransform</i> can point to.

This value must be no less than 1 and no greater than the value specified in <b>historyCount</b> of the <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> structure returned by <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-19fe530f1800">GetPointerInfo</a>, <a href="https://msdn.microsoft.com/97d93754-fc7e-4400-a6ee-6bab53e421cf">GetPointerTouchInfo</a>, or <a href="https://msdn.microsoft.com/5f1f7252-a4aa-4b06-94c9-2aa365cf0100">GetPointerPenInfo</a> (for a single input transform) or <a href="https://msdn.microsoft.com/92173197-45e8-4ee7-8959-2f14f90c2d21">GetPointerInfoHistory</a>, <a href="https://msdn.microsoft.com/9fdfbde7-4126-4c1b-b870-479f846e1aa9">GetPointerTouchInfoHistory</a>, or <a href="https://msdn.microsoft.com/90082327-b242-4f5d-8cd7-fd8ef9340395">GetPointerPenInfoHistory</a> (for an array of input transforms).

If <b>GetPointerInputTransform</b> succeeds, <i>inputTransform</i>  is updated with the total count of structures available. The total count of structures available is the same as the <b>historyCount</b> field of the <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> structure.


### -param inputTransform [out]

Address of an array of <a href="https://msdn.microsoft.com/DE6854F0-17D8-4E4B-97CB-A135910A300C">INPUT_TRANSFORM</a> structures to receive the transform information. This parameter cannot be NULL.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A consumer of pointer input messages typically uses <a href="https://msdn.microsoft.com/5d3e65d1-e0c8-4063-b2e8-dd9f482d3378">ScreenToClient</a> or <a href="https://msdn.microsoft.com/01c3b794-c1ca-467f-a4da-c6622453ee97">MapWindowPoints</a> to convert screen coordinates to client coordinates.

If a transform is applied on the message consumer, use <b>GetPointerInputTransform</b> to retrieve the transform on the message consumer at the time the input occurred. The inverse of this transform can then be used to convert pointer input coordinates from screen coordinates to the client coordinates of the message consumer.

If an input transform is not associated with the input, the <b>GetPointerInputTransform</b> function fails with the last error set to <b>ERROR_NO_DATA</b>. Use <a href="https://msdn.microsoft.com/5d3e65d1-e0c8-4063-b2e8-dd9f482d3378">ScreenToClient</a> or <a href="https://msdn.microsoft.com/01c3b794-c1ca-467f-a4da-c6622453ee97">MapWindowPoints</a> instead.

The input transform does not respect any right-to-left layout setting on the input target. An application that requires adjusted coordinates for right-to-left layout must perform the right-to-left mirroring  or combine an appropriate mirroring transform with the input transform.



The information returned by <b>GetPointerInputTransform</b> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message might no longer be available.

If an application calls <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-19fe530f1800">GetPointerInfo</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and a single <a href="https://msdn.microsoft.com/DE6854F0-17D8-4E4B-97CB-A135910A300C">INPUT_TRANSFORM</a> output buffer to get the input transform associated with the data.

If an application calls <a href="https://msdn.microsoft.com/6b7f450d-6ab1-4991-b2f9-a1db3f065711">GetPointerFrameInfo</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and a single <a href="https://msdn.microsoft.com/DE6854F0-17D8-4E4B-97CB-A135910A300C">INPUT_TRANSFORM</a> output buffer to get the input transform associated with the data. The same input transform applies to the entire frame.

If an application calls <a href="https://msdn.microsoft.com/92173197-45e8-4ee7-8959-2f14f90c2d21">GetPointerInfoHistory</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and an output buffer to hold the entries retrieved using <b>GetPointerInfoHistory</b>. Each input transform in the returned array can be used with the corresponding entry in the array returned by <b>GetPointerInfoHistory</b>.

If an application calls <a href="https://msdn.microsoft.com/1ae035d6-a375-4421-82a6-50be4a2341f6">GetPointerFrameInfoHistory</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and an output buffer to hold the entries retrieved using <a href="https://msdn.microsoft.com/92173197-45e8-4ee7-8959-2f14f90c2d21">GetPointerInfoHistory</a>. Each input transform in the returned array can be used with the corresponding frame in the array returned by <b>GetPointerFrameInfoHistory</b>, with the same input transform being applied to the entire frame.



If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_INVALID_PARAMETER</b>.

If <i>historyCount</i> contains a value larger than the <b>historyCount</b> field of the <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> structure returned by <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-19fe530f1800">GetPointerInfo</a> (or the first <b>POINTER_INFO</b> structure in the array returned by <a href="https://msdn.microsoft.com/92173197-45e8-4ee7-8959-2f14f90c2d21">GetPointerInfoHistory</a>), the function fails with the last error set to <b>ERROR_INVALID_PARAMETER</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/DE6854F0-17D8-4E4B-97CB-A135910A300C">INPUT_TRANSFORM</a>
 

 

