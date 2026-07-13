---
UID: NS:commdlg._OFNOTIFYEXA
title: OFNOTIFYEXA (commdlg.h)
description: Contains information about a CDN_INCLUDEITEM notification message. (ANSI)
helpviewer_keywords: ["*LPOFNOTIFYEXA","LPOFNOTIFYEX","LPOFNOTIFYEX structure pointer [Dialog Boxes]","OFNOTIFYEX","OFNOTIFYEX structure [Dialog Boxes]","OFNOTIFYEXA","OFNOTIFYEXW","_win32_OFNOTIFYEX_str","_win32_ofnotifyex_str_cpp","commdlg/LPOFNOTIFYEX","commdlg/OFNOTIFYEX","commdlg/OFNOTIFYEXA","commdlg/OFNOTIFYEXW","dlgbox.ofnotifyex_str","winui._win32_ofnotifyex_str"]
old-location: dlgbox\ofnotifyex_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\ofnotifyex.htm
ms.date: 12/05/2018
ms.keywords: '*LPOFNOTIFYEXA, LPOFNOTIFYEX, LPOFNOTIFYEX structure pointer [Dialog Boxes], OFNOTIFYEX, OFNOTIFYEX structure [Dialog Boxes], OFNOTIFYEXA, OFNOTIFYEXW, _win32_OFNOTIFYEX_str, _win32_ofnotifyex_str_cpp, commdlg/LPOFNOTIFYEX, commdlg/OFNOTIFYEX, commdlg/OFNOTIFYEXA, commdlg/OFNOTIFYEXW, dlgbox.ofnotifyex_str, winui._win32_ofnotifyex_str'
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OFNOTIFYEXW (Unicode) and OFNOTIFYEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFNOTIFYEXA, *LPOFNOTIFYEXA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OFNOTIFYEXA
 - commdlg/_OFNOTIFYEXA
 - LPOFNOTIFYEXA
 - commdlg/LPOFNOTIFYEXA
 - OFNOTIFYEXA
 - commdlg/OFNOTIFYEXA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commdlg.h
api_name:
 - OFNOTIFYEX
 - OFNOTIFYEXA
 - OFNOTIFYEXW
---

# OFNOTIFYEXA structure


## -description

Contains information about a <a href="/windows/desktop/dlgbox/cdn-includeitem">CDN_INCLUDEITEM</a> notification message.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

The <b>code</b> member of this structure identifies the notification message being sent.

### -field lpOFN

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure containing the values specified when the <b>Open</b> or <b>Save As</b> dialog box was created.

### -field psf

Type: <b>LPVOID</b>

A pointer to the  interface for the folder or shell name-space extension whose items are being enumerated.

### -field pidl

Type: <b>LPVOID</b>

A pointer to an item identifier list that identifies an item in the container identified by the <b>psf</b> member. The item identifier is relative to the <b>psf</b> container.

## -see-also

<a href="/windows/desktop/dlgbox/cdn-includeitem">CDN_INCLUDEITEM</a>



<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a>



<a href="/windows/desktop/api/commdlg/ns-commdlg-ofnotifya">OFNOTIFY</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a>



<b>Reference</b>

## -remarks

> [!NOTE]
> The commdlg.h header defines OFNOTIFYEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
