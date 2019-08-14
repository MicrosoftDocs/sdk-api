---
UID: NF:commdlg.GetSaveFileNameA
title: GetSaveFileNameA function (commdlg.h)
author: windows-sdk-content
description: Creates a Save dialog box that lets the user specify the drive, directory, and name of a file to save.
old-location: dlgbox\getsavefilename.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\getsavefilename.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSaveFileName, GetSaveFileName function [Dialog Boxes], GetSaveFileNameA, GetSaveFileNameW, _win32_GetSaveFileName, _win32_getsavefilename_cpp, commdlg/GetSaveFileName, commdlg/GetSaveFileNameA, commdlg/GetSaveFileNameW, dlgbox.getsavefilename, winui._win32_getsavefilename
ms.topic: function
f1_keywords: 
 - "commdlg/GetSaveFileName"
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSaveFileNameW (Unicode) and GetSaveFileNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comdlg32.dll
 - ext-ms-win-shell-comdlg32-l1-1-0.dll
 - ext-ms-win-shell-comdlg32-l1-1-1.dll
api_name:
 - GetSaveFileName
 - GetSaveFileNameA
 - GetSaveFileNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSaveFileNameA function


## -description


<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Creates a <b>Save</b> dialog box that lets the user specify the drive, directory, and name of a file to save.


## -parameters




### -param Arg1 [in, out]

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="https://docs.microsoft.com/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure that contains information used to initialize the dialog box. When <b>GetSaveFileName</b> returns, this structure contains information about the user's file selection.


## -returns



Type: <b>BOOL</b>

If the user specifies a file name and clicks the 
						<b>OK</b> button and the function is successful, the return value is nonzero. The buffer pointed to by the 
						<b>lpstrFile</b> member of the <a href="https://docs.microsoft.com/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure contains the full path and file name specified by the user.

If the user cancels or closes the 
						<b>Save</b> dialog box or an error such as the file name buffer being too small occurs, the return value is zero. To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a> function, which can return one of the following values: 




## -remarks



The Explorer-style <b>Save</b> dialog box that provides user-interface features that are similar to the Windows Explorer. You can provide an <a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a> hook procedure for an Explorer-style <b>Save</b> dialog box. To enable the hook procedure, set the <b>OFN_EXPLORER</b> and <b>OFN_ENABLEHOOK</b> flags in the  <b>Flags</b> member of the <a href="https://docs.microsoft.com/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure and specify the address of the hook procedure in the  <b>lpfnHook</b> member.

Windows continues to support old-style <b>Save</b> dialog boxes for applications that want to maintain a user-interface consistent with the old-style user-interface. To display the old-style <b>Save</b> dialog box, enable an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)">OFNHookProcOldStyle</a> hook procedure and ensure that the <b>OFN_EXPLORER</b> flag is not set.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/gdi/creating-an-enhanced-metafile">Creating an Enhanced Metafile</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)">OFNHookProcOldStyle</a>



<a href="https://docs.microsoft.com/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a>



<b>Reference</b>
 

 

