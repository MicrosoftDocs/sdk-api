---
UID: NC:msacm.ACMFILTERCHOOSEHOOKPROC
title: ACMFILTERCHOOSEHOOKPROC (msacm.h)
description: The acmFilterChooseHookProc function specifies a user-defined function that hooks the acmFilterChoose dialog box.
helpviewer_keywords: ["_win32_acmFilterChooseHookProc","acmFilterChooseHookProc","acmFilterChooseHookProc callback","acmFilterChooseHookProc callback function [Windows Multimedia]","msacm/acmFilterChooseHookProc","multimedia.acmfilterchoosehookproc"]
old-location: multimedia\acmfilterchoosehookproc.htm
tech.root: Multimedia
ms.assetid: 974bdf53-cd1e-433b-9d49-8dfc20254ebf
ms.date: 12/05/2018
ms.keywords: _win32_acmFilterChooseHookProc, acmFilterChooseHookProc, acmFilterChooseHookProc callback, acmFilterChooseHookProc callback function [Windows Multimedia], msacm/acmFilterChooseHookProc, multimedia.acmfilterchoosehookproc
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
 - ACMFILTERCHOOSEHOOKPROC
 - msacm/ACMFILTERCHOOSEHOOKPROC
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
 - acmFilterChooseHookProc
---

# ACMFILTERCHOOSEHOOKPROC callback function


## -description

The <b>acmFilterChooseHookProc</b> function specifies a user-defined function that hooks the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a> dialog box.

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

To customize the dialog box selections, a hook function can optionally process the MM_ACM_FILTERCHOOSE message.

You should use this function the same way as you use the Common Dialog hook functions for customizing common dialog boxes.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>