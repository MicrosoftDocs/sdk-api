---
UID: NC:commdlg.LPPAGEPAINTHOOK
title: LPPAGEPAINTHOOK (commdlg.h)
description: Receives messages that allow you to customize drawing of the sample page in the Page Setup dialog box. The PagePaintHook hook procedure is an application-defined or library-defined callback function used with the PageSetupDlg function.
helpviewer_keywords: ["LPPAGEPAINTHOOK","LPPAGEPAINTHOOK callback","LPPAGEPAINTHOOK callback function [Dialog Boxes]","_win32_PagePaintHook","_win32_pagepainthook_cpp","commdlg/LPPAGEPAINTHOOK","dlgbox.pagepainthook","winui._win32_pagepainthook"]
old-location: dlgbox\pagepainthook.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\pagepainthook.htm
ms.date: 12/05/2018
ms.keywords: LPPAGEPAINTHOOK, LPPAGEPAINTHOOK callback, LPPAGEPAINTHOOK callback function [Dialog Boxes], _win32_PagePaintHook, _win32_pagepainthook_cpp, commdlg/LPPAGEPAINTHOOK, dlgbox.pagepainthook, winui._win32_pagepainthook
req.header: commdlg.h
req.include-header: Windows.h
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
 - LPPAGEPAINTHOOK
 - commdlg/LPPAGEPAINTHOOK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Commdlg.h
api_name:
 - LPPAGEPAINTHOOK
---

## -description

Receives messages that allow you to customize drawing of the sample page in the <b>Page Setup</b> dialog box. The <i>PagePaintHook</i> hook procedure is an application-defined or library-defined callback function used with the <a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a> function.

The <b>LPPAGEPAINTHOOK</b> type defines a pointer to this callback function. <i>PagePaintHook</i> is a placeholder for the application-defined or library-defined function name.

## -parameters

### -param unnamedParam1

A handle to the <b>Page Setup</b> dialog box.

### -param unnamedParam2

The identifier of the message being received.

### -param unnamedParam3

Additional information about the message. The exact meaning depends on the value of the <i>unnamedParam2</i> parameter.

### -param unnamedParam4

Additional information about the message. The exact meaning depends on the value of the <i>unnamedParam2</i> parameter.

## -returns

If the hook procedure returns <b>TRUE</b> for any of the first three messages of a drawing sequence (<a href="/windows/desktop/dlgbox/wm-psd-pagesetupdlg">WM_PSD_PAGESETUPDLG</a>, <a href="/windows/desktop/dlgbox/wm-psd-fullpagerect">WM_PSD_FULLPAGERECT</a>, or <a href="/windows/desktop/dlgbox/wm-psd-minmarginrect">WM_PSD_MINMARGINRECT</a>), the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page. If the hook procedure returns <b>FALSE</b> for all three messages, the dialog box sends the remaining messages of the drawing sequence.

If the hook procedure returns <b>TRUE</b> for any of the remaining messages in a drawing sequence, the dialog box does not draw the corresponding portion of the sample page. If the hook procedure returns <b>FALSE</b> for any of these messages, the dialog box draws that portion of the sample page.

## -remarks

The <b>Page Setup</b> dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output. The image consists of a rectangle that represents the selected paper or envelope type, with a dotted-line rectangle representing the current margins, and partial (Greek text) characters to show how text looks on the printed page. When you use the <a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a> function to create a <b>Page Setup</b> dialog box, you can provide a <i>PagePaintHook</i> hook procedure to customize the appearance of the sample page.

To enable the hook procedure, use the <a href="/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga">PAGESETUPDLG</a> structure that you passed to the creation function. Specify the pointer to the hook procedure in the  <b>lpfnPagePaintHook</b> member and specify the <b>PSD_ENABLEPAGEPAINTHOOK</b> flag in the  <b>Flags</b> member.

Whenever the dialog box is about to draw the contents of the sample page, the hook procedure receives the following messages in the order in which they are listed.

<table class="clsStd">
<tr>
<th>Message</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/dlgbox/wm-psd-pagesetupdlg">WM_PSD_PAGESETUPDLG</a>
</td>
<td>The dialog box is about to draw the sample page. The hook procedure can use this message to prepare to draw the contents of the sample page.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/dlgbox/wm-psd-fullpagerect">WM_PSD_FULLPAGERECT</a>
</td>
<td>The dialog box is about to draw the sample page. This message specifies the bounding rectangle of the sample page.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/dlgbox/wm-psd-minmarginrect">WM_PSD_MINMARGINRECT</a>
</td>
<td>The dialog box is about to draw the sample page. This message specifies the margin rectangle.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/dlgbox/wm-psd-marginrect">WM_PSD_MARGINRECT</a>
</td>
<td>The dialog box is about to draw the margin rectangle.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/dlgbox/wm-psd-greektextrect">WM_PSD_GREEKTEXTRECT</a>
</td>
<td>The dialog box is about to draw the Greek text inside the margin rectangle.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/dlgbox/wm-psd-envstamprect">WM_PSD_ENVSTAMPRECT</a>
</td>
<td>The dialog box is about to draw in the envelope-stamp rectangle of an envelope sample page. This message is sent for envelopes only.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/dlgbox/wm-psd-yafullpagerect">WM_PSD_YAFULLPAGERECT</a>
</td>
<td>The dialog box is about to draw the return address portion of an envelope sample page. This message is sent for envelopes and other paper sizes.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga">PAGESETUPDLG</a>



<a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a>



<b>Reference</b>