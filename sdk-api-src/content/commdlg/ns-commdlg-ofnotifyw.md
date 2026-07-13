---
UID: NS:commdlg._OFNOTIFYW
title: OFNOTIFYW (commdlg.h)
description: Contains information about a WM_NOTIFY message sent to an OFNHookProc hook procedure for an Open or Save As dialog box. The lParam parameter of the WM_NOTIFY message is a pointer to an OFNOTIFY structure. (Unicode)
helpviewer_keywords: ["*LPOFNOTIFYW","LPOFNOTIFY","LPOFNOTIFY structure pointer [Dialog Boxes]","OFNOTIFY","OFNOTIFY structure [Dialog Boxes]","OFNOTIFYA","OFNOTIFYW","_win32_OFNOTIFY_str","_win32_ofnotify_str_cpp","commdlg/LPOFNOTIFY","commdlg/OFNOTIFY","commdlg/OFNOTIFYA","commdlg/OFNOTIFYW","dlgbox.ofnotify_str","winui._win32_ofnotify_str"]
old-location: dlgbox\ofnotify_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\ofnotify.htm
ms.date: 12/05/2018
ms.keywords: '*LPOFNOTIFYW, LPOFNOTIFY, LPOFNOTIFY structure pointer [Dialog Boxes], OFNOTIFY, OFNOTIFY structure [Dialog Boxes], OFNOTIFYA, OFNOTIFYW, _win32_OFNOTIFY_str, _win32_ofnotify_str_cpp, commdlg/LPOFNOTIFY, commdlg/OFNOTIFY, commdlg/OFNOTIFYA, commdlg/OFNOTIFYW, dlgbox.ofnotify_str, winui._win32_ofnotify_str'
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OFNOTIFYW (Unicode) and OFNOTIFYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OFNOTIFYW
 - commdlg/_OFNOTIFYW
 - LPOFNOTIFYW
 - commdlg/LPOFNOTIFYW
 - OFNOTIFYW
 - commdlg/OFNOTIFYW
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
 - OFNOTIFY
 - OFNOTIFYA
 - OFNOTIFYW
---

# OFNOTIFYW structure


## -description

Contains information about a <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message sent to an <a href="/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a> hook procedure for an <b>Open</b> or <b>Save As</b> dialog box. The <i>lParam</i> parameter of the <b>WM_NOTIFY</b> message is a pointer to an <b>OFNOTIFY</b> structure.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

The <b>code</b> member of this structure can be one of the following notification messages that identify the message being sent: <a href="/windows/desktop/dlgbox/cdn-fileok">CDN_FILEOK</a>, <a href="/windows/desktop/dlgbox/cdn-folderchange">CDN_FOLDERCHANGE</a>, <a href="/windows/desktop/dlgbox/cdn-help">CDN_HELP</a>, <a href="/windows/desktop/dlgbox/cdn-initdone">CDN_INITDONE</a>, <a href="/windows/desktop/dlgbox/cdn-selchange">CDN_SELCHANGE</a>, <a href="/windows/desktop/dlgbox/cdn-shareviolation">CDN_SHAREVIOLATION</a>, <a href="/windows/desktop/dlgbox/cdn-typechange">CDN_TYPECHANGE</a>.

### -field lpOFN

Type: <b>LPOPENFILENAME</b>

A pointer to the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure that was specified when the <b>Open</b> or <b>Save As</b> dialog box was created. For some of the notification messages, this structure contains additional information about the event that caused the notification.

### -field pszFile

Type: <b>LPTSTR</b>

The file name for which a network sharing violation has occurred. This member is valid only with the <a href="/windows/desktop/dlgbox/cdn-shareviolation">CDN_SHAREVIOLATION</a> notification message.

## -remarks

Not all of the <b>Open</b> and <b>Save As</b> notification messages use the <b>OFNOTIFY</b> structure. The <a href="/windows/desktop/dlgbox/cdn-includeitem">CDN_INCLUDEITEM</a> notification message uses the <a href="/windows/desktop/api/commdlg/ns-commdlg-ofnotifyexa">OFNOTIFYEX</a> structure. 





> [!NOTE]
> The commdlg.h header defines OFNOTIFY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dlgbox/cdn-fileok">CDN_FILEOK</a>



<a href="/windows/desktop/dlgbox/cdn-folderchange">CDN_FOLDERCHANGE</a>



<a href="/windows/desktop/dlgbox/cdn-help">CDN_HELP</a>



<a href="/windows/desktop/dlgbox/cdn-initdone">CDN_INITDONE</a>



<a href="/windows/desktop/dlgbox/cdn-selchange">CDN_SELCHANGE</a>



<a href="/windows/desktop/dlgbox/cdn-shareviolation">CDN_SHAREVIOLATION</a>



<a href="/windows/desktop/dlgbox/cdn-typechange">CDN_TYPECHANGE</a>



<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/ns-commdlg-ofnotifyexa">OFNOTIFYEX</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a>



<b>Reference</b>
