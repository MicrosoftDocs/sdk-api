---
UID: NF:winuser.InjectTouchInput
title: InjectTouchInput function
author: windows-sdk-content
description: Simulates touch input.
old-location: input_touchinjection\injecttouchinput.htm
tech.root: Input_TouchInjection
ms.assetid: c3c1425e-2af6-4ecb-a0b2-a456654f7a53
ms.author: windowssdkdev
ms.date: 10/11/2018
ms.keywords: InjectTouchInput, InjectTouchInput function [Windows Touch], input_touchinjection.injecttouchinput, touch_injection.injecttouchinput, winuser/InjectTouchInput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: 
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
 - user32.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - InjectTouchInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InjectTouchInput function


## -description


Simulates touch input.<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/79cc2a05-d8ee-4d87-9c7b-fa7d5354b04f">InitializeTouchInjection</a> must precede any call to  <a href="https://msdn.microsoft.com/c3c1425e-2af6-4ecb-a0b2-a456654f7a53">InjectTouchInput</a>.</div>
<div> </div>



## -parameters




### -param count [in]

The size of the array in <i>contacts</i>. 

The maximum value for <i>count</i> is specified by the <i>maxCount</i> parameter of the <a href="https://msdn.microsoft.com/79cc2a05-d8ee-4d87-9c7b-fa7d5354b04f">InitializeTouchInjection</a> function.


### -param contacts [in]

Array of <a href="https://msdn.microsoft.com/fee176ba-ad07-3141-ab4d-1b8c335fd102">POINTER_TOUCH_INFO</a> structures that represents all contacts on the desktop. The  screen coordinates of each contact must be within the bounds of the desktop.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The injected input is sent to the desktop of the session where the injection process is running.

There are two input states for touch input injection (interactive and hover) that are indicated by the following combinations of <b>pointerFlags</b> in <i>contacts</i>:

<table>
<tr>
<th><b>pointerFlags (POINTER_FLAG_*)</b></th>
<th>Status</th>
</tr>
<tr>
<td>INRANGE | UPDATE</td>
<td>Touch hover starts or moves</td>
</tr>
<tr>
<td>INRANGE | INCONTACT | DOWN</td>
<td>Touch contact down</td>
</tr>
<tr>
<td>INRANGE | INCONTACT | UPDATE </td>
<td>Touch contact moves</td>
</tr>
<tr>
<td>INRANGE | UP</td>
<td>Touch contact up and transition to hover</td>
</tr>
<tr>
<td>UPDATE</td>
<td>Touch hover ends</td>
</tr>
<tr>
<td>UP</td>
<td>Touch ends</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Interactive state represents a touch contact that is on-screen and able to interact with any touch-capable app. Hover state represents touch input that  is not  in contact with the screen and cannot interact with applications. Touch injection can start in hover or interactive state, but the state can only transition through INRANGE | INCONTACT | DOWN for hover to  interactive state, or through INRANGE | UP for interactive to hover state.</div>
<div> </div>
All touch injection sequences end with either UPDATE or UP.

The following diagram demonstrates a touch injection sequence that starts with a hover state, transitions to interactive, and concludes with hover. 

<img alt="" src="./images/inputstates.png"/>

For press and hold gestures, multiple frames must be sent to ensure input is not cancelled. For a press and hold at point (x,y), send <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> at point (x,y) followed by <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac222">WM_POINTERUPDATE</a> messages at point(x,y). 

Listen for <a href="https://msdn.microsoft.com/5a6111fd-648e-41a9-aaf8-e5d93f5d54cd">WM_DISPLAYCHANGE</a> to handle changes to display resolution and orientation and manage screen coordinate updates. All active contacts are cancelled when a <b>WM_DISPLAYCHANGE</b> is received.

Cancel individual contacts by setting POINTER_FLAG_CANCELED with POINTER_FLAG_UP or POINTER_FLAG_UPDATE. Cancelling touch injection without POINTER_FLAG_UP or POINTER_FLAG_UPDATE invalidates the injection.

When POINTER_FLAG_UP is set, ptPixelLocation of <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> should be the same as the value of the previous touch injection frame with POINTER_FLAG_UPDATE. Otherwise, the injection fails with ERROR_INVALID_PARAMETER and all active injection contacts are cancelled. The system modifies the ptPixelLocation of the <a href="https://msdn.microsoft.com/3bdc38da-227c-4be1-bf0b-99704b8a0111">WM_POINTERUP</a> event as it cancels the injection. 

The input timestamp can be specified in either the dwTime or PerformanceCount field of <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a>. The value cannot be more recent than the current tick count or <a href="https://msdn.microsoft.com/08169390-940b-4110-813a-249d107cc953">QueryPerformanceCounter</a> value of the injection thread. Once a frame is injected with a timestamp, all subsequent frames must include a timestamp until all contacts in the frame go to the UP state. The custom timestamp value must be provided for the first element in the contacts array. The timestamp values after the first element are ignored. The custom timestamp value must increment in every injection frame.



When a PerformanceCount field is specified, the timestamp is converted into current time in .1 millisecond resolution upon actual injection. If a custom PerformanceCount resulted in the same .1 millisecond window from previous injection, the API will return an error (ERROR_NOT_READY) and will not inject the data. While injection is not immediately invalidated by the error, next successful injection must have PerformanceCount value that is at least 0.1 milliseconds apart from the previously successful injection. Similarly a custom dwTime value must be at least 1 millisecond apart if the field was used.



If both dwTime and PerformanceCount are specified in the injection parameter, <a href="https://msdn.microsoft.com/c3c1425e-2af6-4ecb-a0b2-a456654f7a53">InjectTouchInput</a> fails with an Error Code (ERROR_INVALID_PARAMETER). Once the injection application starts with either a dwTime or PerformanceCount parameter, the timestamp field must be filled correctly. Injection cannot switch the custom timestamp field from one to another once the injection sequence  has started.



When neither dwTime or PerformanceCount values are specified, the <a href="https://msdn.microsoft.com/c3c1425e-2af6-4ecb-a0b2-a456654f7a53">InjectTouchInput</a> allocates the timestamp based on the timing of the API call. If the calls are less than 0.1 millisecond apart, the API may return an error (ERROR_NOT_READY). The error will not invalidate the input immediately, but the injection application needs to retry the same frame again to ensure  injection is successful.





## -see-also




<a href="https://msdn.microsoft.com/c1533555-9094-0030-f025-6f47e9002e1a">Functions</a>
 

 

