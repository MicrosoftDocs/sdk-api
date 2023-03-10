---
UID: NC:msacm.ACMFORMATCHOOSEHOOKPROC
title: ACMFORMATCHOOSEHOOKPROC (msacm.h)
description: The acmFormatChooseHookProc function specifies a user-defined function that hooks the acmFormatChoose dialog box. The acmFormatChooseHookProc name is a placeholder for an application-defined name.
helpviewer_keywords: ["_win32_acmFormatChooseHookProc","acmFormatChooseHookProc","acmFormatChooseHookProc callback","acmFormatChooseHookProc callback function [Windows Multimedia]","msacm/acmFormatChooseHookProc","multimedia.acmformatchoosehookproc"]
old-location: multimedia\acmformatchoosehookproc.htm
tech.root: Multimedia
ms.assetid: 75b11c0f-ae85-424d-b936-492d67440659
ms.date: 12/05/2018
ms.keywords: _win32_acmFormatChooseHookProc, acmFormatChooseHookProc, acmFormatChooseHookProc callback, acmFormatChooseHookProc callback function [Windows Multimedia], msacm/acmFormatChooseHookProc, multimedia.acmformatchoosehookproc
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
 - ACMFORMATCHOOSEHOOKPROC
 - msacm/ACMFORMATCHOOSEHOOKPROC
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
 - acmFormatChooseHookProc
---

# ACMFORMATCHOOSEHOOKPROC callback function


## -description

The <b>acmFormatChooseHookProc</b> function specifies a user-defined function that hooks the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a> dialog box. The <b>acmFormatChooseHookProc</b> name is a placeholder for an application-defined name.

## -parameters

### -param hwnd

Window handle for the dialog box.

### -param uMsg

Window message.

### -param wParam

Message parameter.

### -param lParam

Message parameter.

## -remarks

If the hook function processes one of the WM_CTLCOLOR messages, this function must return a handle of the brush that should be used to paint the control background.

A hook function can optionally process the MM_ACM_FORMATCHOOSE message.

You should use this function the same way as you use the Common Dialog hook functions for customizing common dialog boxes.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>