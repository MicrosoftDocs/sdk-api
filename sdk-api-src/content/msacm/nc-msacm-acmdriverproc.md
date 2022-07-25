---
UID: NC:msacm.ACMDRIVERPROC
title: ACMDRIVERPROC (msacm.h)
description: The acmDriverProc function specifies a callback function used with the ACM driver.
helpviewer_keywords: ["_win32_acmDriverProc","acmDriverProc","acmDriverProc callback","acmDriverProc callback function [Windows Multimedia]","msacm/acmDriverProc","multimedia.acmdriverproc"]
old-location: multimedia\acmdriverproc.htm
tech.root: Multimedia
ms.assetid: e29c157d-e56e-4242-abb8-2736d5599caa
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverProc, acmDriverProc, acmDriverProc callback, acmDriverProc callback function [Windows Multimedia], msacm/acmDriverProc, multimedia.acmdriverproc
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ACMDRIVERPROC
 - msacm/ACMDRIVERPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - acmDriverProc
---

# ACMDRIVERPROC callback function


## -description

The <b>acmDriverProc</b> function specifies a callback function used with the ACM driver. The <b>acmDriverProc</b> name is a placeholder for an application-defined function name. The actual name must be exported by including it in the module-definition file of the executable or DLL file.

## -parameters

### -param unnamedParam1

Identifier of the installable ACM driver.

### -param unnamedParam2

Handle to the installable ACM driver. This parameter is a unique handle the ACM assigns to the driver.

### -param unnamedParam3

ACM driver message.

### -param unnamedParam4

Message parameter.

### -param unnamedParam5

Message parameter.


## -returns

Returns zero if successful or an error otherwise.

## -remarks

Applications should not call any system-defined functions from inside a callback function, except for <b>PostMessage</b>, <a href="/windows/desktop/api/timeapi/nf-timeapi-timegetsystemtime">timeGetSystemTime</a>, <a href="/windows/desktop/api/timeapi/nf-timeapi-timegettime">timeGetTime</a>, <a href="/previous-versions/dd757634(v=vs.85)">timeSetEvent</a>, <a href="/previous-versions/dd757630(v=vs.85)">timeKillEvent</a>, <a href="/previous-versions/dd798481(v=vs.85)">midiOutShortMsg</a>, <a href="/previous-versions/dd798474(v=vs.85)">midiOutLongMsg</a>, and <b>OutputDebugStr</b>.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>