---
UID: NF:winuser.GetPointerTouchInfoHistory
title: GetPointerTouchInfoHistory function
author: windows-sdk-content
description: Gets the touch-based information associated with the individual inputs, if any, that were coalesced into the current message for the specified pointer (of type PT_TOUCH).
old-location: inputmsg\getpointertouchinfohistory.htm
old-project: InputMsg
ms.assetid: 9fdfbde7-4126-4c1b-b870-479f846e1aa9
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetPointerTouchInfoHistory, GetPointerTouchInfoHistory function [Input Messages and Notifications], inputmsg.getpointertouchinfohistory, winuser/GetPointerTouchInfoHistory
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
 - GetPointerTouchInfoHistory
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPointerTouchInfoHistory function


## -description


Gets the touch-based information associated with the individual inputs, if any, that were coalesced into the current message for the specified pointer (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>). The most recent input is included in the returned history and is the same as the most recent input returned by the <a href="https://msdn.microsoft.com/97d93754-fc7e-4400-a6ee-6bab53e421cf">GetPointerTouchInfo</a> function.


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve information.


### -param entriesCount [in, out]

A pointer to a variable that specifies the count of structures in the buffer to which touchInfo points. If <b>GetPointerTouchInfoHistory</b> succeeds, <i>entriesCount</i> is updated with the total count of structures available. The total count of structures available is the same as the <i>historyCount</i> field in the <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> structure returned by a call to <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-19fe530f1800">GetPointerInfo</a> or <a href="https://msdn.microsoft.com/97d93754-fc7e-4400-a6ee-6bab53e421cf">GetPointerTouchInfo</a>.


### -param touchInfo [out, optional]

Address of an array of <a href="https://msdn.microsoft.com/fee176ba-ad07-3141-ab4d-1b8c335fd102">POINTER_TOUCH_INFO</a> structures to receive the pointer information. This parameter can be NULL if *entriesCount is zero.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the application does not process pointer input messages as fast as they are generated, some moves may be coalesced. When an application receives a coalescable pointer (of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>) message, it can use the <b>GetPointerTouchInfoHistory</b> function to retrieve information for all the individual inputs, if any, that were coalesced into the message. Note that the information retrieved is associated with the pointer message most recently retrieved by the calling thread. Once the calling thread retrieves its next message, the information associated with the previous message may no longer be available.

The information retrieved appears in reverse chronological order, with the most recent entry in the first row of the returned array. The most recent entry is the same as that returned by the <a href="https://msdn.microsoft.com/97d93754-fc7e-4400-a6ee-6bab53e421cf">GetPointerTouchInfo</a> function.

If the count of rows in the buffer provided is insufficient to hold all available history entries, this function succeeds with the buffer containing the most recent entries and <i>*entriesCount</i> containing the total count of entries available.


If the pointer frame contains no additional pointers besides the specified pointer, this function succeeds and returns only the information for the specified pointer.

If the information associated with the pointer frame is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window (where the input was originally delivered or where the message was forwarded) to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. 

If the specified pointer is not of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.






## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/a100cc7a-62fc-4ace-8d35-e77aff98d944">GetPointerFrameTouchInfo</a>



<a href="https://msdn.microsoft.com/f2521a67-9850-46e9-bc8b-75bf5b6cc263">GetPointerFrameTouchInfoHistory</a>



<a href="https://msdn.microsoft.com/97d93754-fc7e-4400-a6ee-6bab53e421cf">GetPointerTouchInfo</a>
 

 

