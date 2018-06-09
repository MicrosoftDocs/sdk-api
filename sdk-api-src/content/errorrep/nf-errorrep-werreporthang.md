---
UID: NF:errorrep.WerReportHang
title: WerReportHang function
author: windows-sdk-content
description: Initiates &#0034;no response&#0034; reporting on the specified window.
old-location: wer\werreporthang.htm
old-project: wer
ms.assetid: db147395-4d60-4d74-9331-18137bcfff8e
ms.author: windowssdkdev
ms.date: 03/22/2018
ms.keywords: WerReportHang, WerReportHang function [Windows Error Reporting], errorrep/WerReportHang, wer.werreporthang
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: errorrep.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Faultrep.dll
api_name:
 - WerReportHang
product: Windows
targetos: Windows
req.lib: Faultrep.lib
req.dll: Faultrep.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# WerReportHang function


## -description


Initiates "no response" reporting on the specified window.


## -parameters




### -param hwndHungApp

TBD


### -param pwzHungApplicationName

TBD




#### - hwndHungWindow [in]

Handle to the window that is not responding.


#### - wszHungApplicationName [in, optional]

The name of the not-responding application to be shown in the Hang Reporting UI. The name is limited to 128 characters including the <b>NULL</b> terminator. If <b>NULL</b>, WER tries to get the name from the target image resources. If it cannot get the name from the image, the image name will be used.


## -returns



Returns S_OK if the function was able to initiate the reporting or an error code on failure. Note that S_OK does not necessarily mean that "no response" reporting has completed successfully, only that it was initiated.




## -remarks



<div class="alert"><b>Caution</b>  Applications should not use this API to report no response from top-level windows; no-response detection and reporting is available to all top-level windows on Windows XP and later by default. You should only use this function to report no response from child windows. Typically, you would use this function only when the top-level window and its child windows are owned by different processes and a non-response is detected in a child window.</div>
<div> </div>
This function will initiate no-response reporting which will then terminate the process that created the window. The caller is responsible for determining when a child window is not responding and should prompt the user for consent before reporting the non-response. A typical way to detect a window that is not responding is to check that it replies to window messages in a timely manner. You can use the <b>SendMessageTimeout</b> function to detect this condition.

This function is asynchronous; it does not wait for no-response reporting to complete. There is no way to cancel no-response reporting after it is started.

If you use this function, it is important that you adhere to the following requirements:

<ul>
<li>Ensure that child windows are created by a separate process. After no-response reporting has completed, it will terminate the process that created the window.</li>
<li>Provide visual clues in the child window that it is not responding; no-response reporting will not dim the child window, it will only show the reporting dialog box.</li>
<li>Confirm that the user wants to terminate the child window that is not responding before calling this function.</li>
<li>To have the no-response reporting UI appear in front of the window that is not responding, the application should call the <a href="_win32_allowsetforegroundwindow_cpp">AllowSetForegroundWindow</a> (passing ASFW_ANY for the process identifier) function from the top-level window's process.</li>
</ul>


