---
UID: NC:msacm.ACMDRIVERPROC
title: ACMDRIVERPROC (msacm.h)
author: windows-sdk-content
description: The acmDriverProc function specifies a callback function used with the ACM driver.
old-location: multimedia\acmdriverproc.htm
tech.root: Multimedia
ms.assetid: e29c157d-e56e-4242-abb8-2736d5599caa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_acmDriverProc, acmDriverProc, acmDriverProc callback, acmDriverProc callback function [Windows Multimedia], msacm/acmDriverProc, multimedia.acmdriverproc"
ms.topic: callback
f1_keywords: 
 - "msacm/acmDriverProc"
dev_langs:
 - c++
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - acmDriverProc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ACMDRIVERPROC callback function


## -description



The <b>acmDriverProc</b> function specifies a callback function used with the ACM driver. The <b>acmDriverProc</b> name is a placeholder for an application-defined function name. The actual name must be exported by including it in the module-definition file of the executable or DLL file.




## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4


### -param Arg5








#### - dwID

Identifier of the installable ACM driver.


#### - hdrvr

Handle to the installable ACM driver. This parameter is a unique handle the ACM assigns to the driver.


#### - lParam1

Message parameter.


#### - lParam2

Message parameter.


#### - uMsg

ACM driver message.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



Applications should not call any system-defined functions from inside a callback function, except for <b>PostMessage</b>, <a href="https://docs.microsoft.com/windows/desktop/api/timeapi/nf-timeapi-timegetsystemtime">timeGetSystemTime</a>, <a href="https://docs.microsoft.com/windows/desktop/api/timeapi/nf-timeapi-timegettime">timeGetTime</a>, <a href="https://docs.microsoft.com/previous-versions/dd757634(v=vs.85)">timeSetEvent</a>, <a href="https://docs.microsoft.com/previous-versions/dd757630(v=vs.85)">timeKillEvent</a>, <a href="https://docs.microsoft.com/previous-versions/dd798481(v=vs.85)">midiOutShortMsg</a>, <a href="https://docs.microsoft.com/previous-versions/dd798474(v=vs.85)">midiOutLongMsg</a>, and <b>OutputDebugStr</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
 

 

