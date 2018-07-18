---
UID: NF:winbio.WinBioAcquireFocus
title: WinBioAcquireFocus function
author: windows-sdk-content
description: Acquires window focus.
old-location: secbiomet\winbioacquirefocus.htm
old-project: secbiomet
ms.assetid: ad8bdcc9-0317-4d35-a587-9a2f3a4144ae
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: WinBioAcquireFocus, WinBioAcquireFocus function [Windows Biometric Framework API], secbiomet.winbioacquirefocus, winbio/WinBioAcquireFocus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbio.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - WinBioExt.dll
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-L1-3-0.dll
api_name:
 - WinBioAcquireFocus
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioAcquireFocus function


## -description


Acquires window focus.


## -parameters






## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process must be running under the Local System account.

</td>
</tr>
</table>
 




## -remarks



The Windows Biometric Framework uses window focus to arbitrate among multiple sessions connected to  the system pool.

The manner in which you acquire focus depends on the type of application you are writing. For example, if you are creating a GUI application you can implement a message handler that captures  a <a href="https://msdn.microsoft.com/library/ms646274(v=VS.85).aspx">WM_ACTIVATE</a>, <a href="https://msdn.microsoft.com/library/ms646283(v=VS.85).aspx">WM_SETFOCUS</a>, or other appropriate message. If you are writing a CUI application, call <b>GetConsoleWindow</b> to retrieve a handle to the console window and pass that handle to the <b>SetForegroundWindow</b> function to force the console window into the foreground and assign it focus. If your application is running in a detached process or is a Windows service and has no window, use <b>WinBioAcquireFocus</b> and <a href="https://msdn.microsoft.com/260f24e9-4527-4bec-b18a-64781060714b">WinBioReleaseFocus</a> to manually control focus.

The following list summarizes the major points to consider before calling this function.

<ul>
<li>The calling process must be running under the Local System account.</li>
<li>A process that directly displays a user interface should not call this function. See the preceding discussion to determine how to acquire focus for GUI and CUI applications.</li>
<li>Only a service or a detached process that does not directly display a user interface during biometric API calls should call this function.</li>
<li>If the function succeeds, you must call <a href="https://msdn.microsoft.com/260f24e9-4527-4bec-b18a-64781060714b">WinBioReleaseFocus</a> to release focus.</li>
</ul>
If you do not acquire focus when calling the following functions, they will behave in unexpected ways:

<ul>
<li>
<a href="https://msdn.microsoft.com/ee706f2a-f544-4f53-b776-064d32e8acc8">WinBioEnrollBegin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a50f0c9f-7b9c-4d80-b8fc-8b83bc333578">WinBioEnrollCapture</a>
</li>
<li>
<a href="https://msdn.microsoft.com/809e7d2f-6b41-4afc-86c2-43b6611d6e48">WinBioEnrollCaptureWithCallback</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/57c9378d-b170-4ba8-8eee-8078531540d5">Client Application Functions</a>



<a href="https://msdn.microsoft.com/ee706f2a-f544-4f53-b776-064d32e8acc8">WinBioEnrollBegin</a>
 

 

