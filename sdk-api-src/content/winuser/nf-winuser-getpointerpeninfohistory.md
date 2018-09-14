---
UID: NF:winuser.GetPointerPenInfoHistory
title: GetPointerPenInfoHistory function
author: windows-sdk-content
description: Gets the pen-based information associated with the individual inputs, if any, that were coalesced into the current message for the specified pointer (of type PT_PEN).
old-location: inputmsg\getpointerpeninfohistory.htm
tech.root: InputMsg
ms.assetid: 90082327-b242-4f5d-8cd7-fd8ef9340395
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetPointerPenInfoHistory, GetPointerPenInfoHistory function [Input Messages and Notifications], inputmsg.getpointerpeninfohistory, winuser/GetPointerPenInfoHistory
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
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerPenInfoHistory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPointerPenInfoHistory function


## -description


Gets the pen-based information associated with the individual inputs, if any, that were coalesced into 
    the current message for the specified pointer (of type 
    <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a>). The most recent input is included in 
    the returned history and is the same as the most recent input returned by the 
    <a href="https://msdn.microsoft.com/5f1f7252-a4aa-4b06-94c9-2aa365cf0100">GetPointerPenInfo</a> function.


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve information.


### -param entriesCount [in, out]

A pointer to a variable that specifies the count of structures in the buffer to which 
       <i>penInfo</i> points. If 
       <b>GetPointerPenInfoHistory</b> succeeds, 
       <i>entriesCount</i> is updated with the total count of structures available. The total 
       count of structures available is the same as the <i>historyCount</i> field in the 
       <a href="https://msdn.microsoft.com/fee176ba-ad07-4141-ab4d-1b8c335fd111">POINTER_PEN_INFO</a> structure returned by a 
       call to  <a href="https://msdn.microsoft.com/5f1f7252-a4aa-4b06-94c9-2aa365cf0100">GetPointerPenInfo</a>.


### -param penInfo [out, optional]

Address of an array of 
       <a href="https://msdn.microsoft.com/fee176ba-ad07-4141-ab4d-1b8c335fd111">POINTER_PEN_INFO</a> structures to receive 
       the pointer information. This parameter can be NULL if <i>*entriesCount</i> is zero.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the application does not process pointer input messages as fast as they are generated, some moves may be 
    coalesced. When an application receives a coalescable pointer (of type 
    <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a>) message, it can use the 
    <b>GetPointerPenInfoHistory</b> function to 
    retrieve information for all the individual inputs, if any, that were coalesced into the message. Note that the 
    information retrieved is associated with the pointer message most recently retrieved by the calling thread. Once 
    the calling thread retrieves its next message, the information associated with the previous message may no longer 
    be available.

The information retrieved appears in reverse chronological order, with the most recent 
    entry in the first row of the returned array. The most recent entry is the same as that returned by the 
    <a href="https://msdn.microsoft.com/5f1f7252-a4aa-4b06-94c9-2aa365cf0100">GetPointerPenInfo</a> function.

If the count of rows in the buffer provided is insufficient to hold all available history entries, this 
    function succeeds with the buffer containing the most recent entries and <i>*entriesCount</i> 
    containing the total count of entries available.

If the pointer frame contains no additional pointers besides the specified pointer, this function succeeds and 
    returns only the information for the specified pointer.

If the information associated with the pointer frame is no longer available, this function fails with the last 
    error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window (where the input was originally delivered or where the message 
    was forwarded) to which the pointer message has been delivered, this function fails with the last error set to 
    <b>ERROR_ACCESS_DENIED</b>.

If the specified pointer is not of type 
    <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a>, this function fails with the last 
     error set to <b>ERROR_DATATYPE_MISMATCH</b>.




## -see-also




<a href="https://msdn.microsoft.com/0123DCD0-DAE1-4AC2-AB36-23D114803138">Functions</a>



<a href="https://msdn.microsoft.com/52db9b96-7f9e-41d7-88f7-b9c7691a6511">GetPointerFramePenInfo</a>



<a href="https://msdn.microsoft.com/a4f6a9f3-dfbd-4413-aae7-f58e1521ef1d">GetPointerFramePenInfoHistory</a>



<a href="https://msdn.microsoft.com/5f1f7252-a4aa-4b06-94c9-2aa365cf0100">GetPointerPenInfo</a>
 

 

