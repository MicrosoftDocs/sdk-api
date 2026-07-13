---
UID: NF:commdlg.GetOpenFileNameW
title: GetOpenFileNameW function (commdlg.h)
description: Creates an Open dialog box that lets the user specify the drive, directory, and the name of a file or set of files to be opened. (Unicode)
helpviewer_keywords: ["GetOpenFileName", "GetOpenFileName function [Dialog Boxes]", "GetOpenFileNameW", "_win32_GetOpenFileName", "_win32_getopenfilename_cpp", "commdlg/GetOpenFileName", "commdlg/GetOpenFileNameW", "dlgbox.getopenfilename", "winui._win32_getopenfilename"]
old-location: dlgbox\getopenfilename.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\getopenfilename.htm
ms.date: 12/05/2018
ms.keywords: GetOpenFileName, GetOpenFileName function [Dialog Boxes], GetOpenFileNameA, GetOpenFileNameW, _win32_GetOpenFileName, _win32_getopenfilename_cpp, commdlg/GetOpenFileName, commdlg/GetOpenFileNameA, commdlg/GetOpenFileNameW, dlgbox.getopenfilename, winui._win32_getopenfilename
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetOpenFileNameW (Unicode) and GetOpenFileNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetOpenFileNameW
 - commdlg/GetOpenFileNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comdlg32.dll
 - ext-ms-win-shell-comdlg32-l1-1-0.dll
api_name:
 - GetOpenFileName
 - GetOpenFileNameA
 - GetOpenFileNameW
req.apiset: ext-ms-win-shell-comdlg32-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# GetOpenFileNameW function


## -description

<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="/windows/win32/shell/common-file-dialog">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Creates an <b>Open</b> dialog box that lets the user specify the drive, directory, and the name of a file or set of files to be opened.

## -parameters

### -param unnamedParam1 [in, out]

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure that contains information used to initialize the dialog box. When <b>GetOpenFileName</b> returns, this structure contains information about the user's file selection.

## -returns

Type: <b>BOOL</b>

If the user specifies a file name and clicks the <b>OK</b> button, the return value is nonzero. The buffer pointed to by the <b>lpstrFile</b> member of the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure contains the full path and file name specified by the user.

If the user cancels or closes the <b>Open</b> dialog box or an error occurs, the return value is zero. To get extended error information, call the <a href="/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a> function, which can return one of the following values.

## -remarks

The Explorer-style <b>Open</b> dialog box provides user-interface features that are similar to the Windows Explorer. You can provide an <a href="/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a> hook procedure for an Explorer-style <b>Open</b> dialog box. To enable the hook procedure, set the <b>OFN_EXPLORER</b> and <b>OFN_ENABLEHOOK</b> flags in the <b>Flags</b> member of the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure and specify the address of the hook procedure in the <b>lpfnHook</b> member.

Windows continues to support the old-style <b>Open</b> dialog box for applications that want to maintain a user-interface consistent with the old-style user-interface. To display the old-style <b>Open</b> dialog box, enable an <a href="/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)">OFNHookProcOldStyle</a> hook procedure and ensure that the <b>OFN_EXPLORER</b> flag is not set.

To display a dialog box that allows the user to select a directory instead of a file, call the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a> function.

Note, when selecting multiple files, the total character limit for the file names depends on the version of the function.

<ul>
<li>ANSI: 32k limit</li>
<li>Unicode: no restriction </li>
</ul>

#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-common-dialog-boxes">Opening a File</a>.

<div class="code"></div>




> [!NOTE]
> The commdlg.h header defines GetOpenFileName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a>



<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a>



<a href="/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a>



<a href="/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)">OFNHookProcOldStyle</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a>
