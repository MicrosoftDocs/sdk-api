---
UID: NF:winuser.SetUserObjectInformationA
title: SetUserObjectInformationA function
author: windows-sdk-content
description: Sets information about the specified window station or desktop object.
old-location: winstation\setuserobjectinformation.htm
tech.root: winstation
ms.assetid: 42ce6946-1659-41a3-8ba7-21588583b4bd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetUserObjectInformation, SetUserObjectInformation function [Windows Stations and Desktops], SetUserObjectInformationA, SetUserObjectInformationW, UOI_FLAGS, UOI_TIMERPROC_EXCEPTION_SUPPRESSION, _win32_setuserobjectinformation, base.setuserobjectinformation, winstation.setuserobjectinformation, winuser/SetUserObjectInformation, winuser/SetUserObjectInformationA, winuser/SetUserObjectInformationW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetUserObjectInformationW (Unicode) and SetUserObjectInformationA (ANSI)
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
api_name:
 - SetUserObjectInformation
 - SetUserObjectInformationA
 - SetUserObjectInformationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetUserObjectInformationA function


## -description


Sets information about the specified window station or desktop object.


## -parameters




### -param hObj [in]

A handle to the window station, desktop object or a current process pseudo handle. This handle can be returned by the  <a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>, 
<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>, 
<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>, <a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a> or  <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> function.


### -param nIndex [in]

The object information to be set. This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UOI_FLAGS"></a><a id="uoi_flags"></a><dl>
<dt><b>UOI_FLAGS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Sets the object's handle flags. The <i>pvInfo</i> parameter must point to a 
<a href="https://msdn.microsoft.com/5a973d45-5ff4-47e7-a927-72d3fdd61dc9">USEROBJECTFLAGS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="UOI_TIMERPROC_EXCEPTION_SUPPRESSION"></a><a id="uoi_timerproc_exception_suppression"></a><dl>
<dt><b>UOI_TIMERPROC_EXCEPTION_SUPPRESSION</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Sets the exception handling behavior when calling <a href="https://msdn.microsoft.com/en-us/library/ms644907(v=VS.85).aspx">TimerProc</a>.
 <i>hObj</i> must be the process handle returned by the <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> function.
 

The <i>pvInfo</i> parameter must point to a BOOL.  If TRUE, Windows will enclose its calls to <a href="https://msdn.microsoft.com/en-us/library/ms644907(v=VS.85).aspx">TimerProc</a> with an exception handler that consumes and discards all exceptions. This has been the default behavior since Windows 2000, although that may change in future versions of Windows.  

If <i>pvInfo</i>  points to FALSE, Windows will not enclose its calls to <a href="https://msdn.microsoft.com/en-us/library/ms644907(v=VS.85).aspx">TimerProc</a> with an exception handler. A setting of FALSE is recommended.  Otherwise, the application could behave unpredictably, and could be more vulnerable to security exploits.

</td>
</tr>
</table>
 


### -param pvInfo [in]

A pointer to a buffer containing the object information, or a BOOL.


### -param nLength [in]

The size of the information contained in the buffer pointed to by <i>pvInfo</i>, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>



<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>



<a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a>



<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>



<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>



<a href="https://msdn.microsoft.com/5a973d45-5ff4-47e7-a927-72d3fdd61dc9">USEROBJECTFLAGS</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>



<a href="https://msdn.microsoft.com/617661e2-3b0d-42a9-9769-2ba0957c31a8">Window Stations</a>
 

 

