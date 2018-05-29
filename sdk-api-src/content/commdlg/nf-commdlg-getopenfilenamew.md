---
UID: NF:commdlg.GetOpenFileNameW
title: GetOpenFileNameW function
author: windows-sdk-content
description: Creates an Open dialog box that lets the user specify the drive, directory, and the name of a file or set of files to be opened.
old-location: dlgbox\getopenfilename.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\getopenfilename.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetOpenFileName, GetOpenFileName function [Dialog Boxes], GetOpenFileNameA, GetOpenFileNameW, _win32_GetOpenFileName, _win32_getopenfilename_cpp, commdlg/GetOpenFileName, commdlg/GetOpenFileNameA, commdlg/GetOpenFileNameW, dlgbox.getopenfilename, winui._win32_getopenfilename
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: UDACCEL, *LPUDACCEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comdlg32.dll
-	ext-ms-win-shell-comdlg32-l1-1-0.dll
api_name:
-	GetOpenFileName
-	GetOpenFileNameA
-	GetOpenFileNameW
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll
req.irql: 
---

# GetOpenFileNameW function


## -description


<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="_shell_common_file_dialog">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Creates an <b>Open</b> dialog box that lets the user specify the drive, directory, and the name of a file or set of files to be opened.


## -parameters




### -param Arg1

TBD




#### - lpofn [in, out]

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure that contains information used to initialize the dialog box. When <b>GetOpenFileName</b> returns, this structure contains information about the user's file selection.


## -returns



Type: <b>BOOL</b>

If the user specifies a file name and clicks the <b>OK</b> button, the return value is nonzero. The buffer pointed to by the <b>lpstrFile</b> member of the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure contains the full path and file name specified by the user.

If the user cancels or closes the <b>Open</b> dialog box or an error occurs, the return value is zero. To get extended error information, call the <a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a> function, which can return one of the following values.




## -remarks



The Explorer-style <b>Open</b> dialog box provides user-interface features that are similar to the Windows Explorer. You can provide an <a href="https://msdn.microsoft.com/3d3a7878-1ccc-4832-9351-8f9cf6c7a601">OFNHookProc</a> hook procedure for an Explorer-style <b>Open</b> dialog box. To enable the hook procedure, set the <b>OFN_EXPLORER</b> and <b>OFN_ENABLEHOOK</b> flags in the <b>Flags</b> member of the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure and specify the address of the hook procedure in the <b>lpfnHook</b> member.

Windows continues to support the old-style <b>Open</b> dialog box for applications that want to maintain a user-interface consistent with the old-style user-interface. To display the old-style <b>Open</b> dialog box, enable an <a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a> hook procedure and ensure that the <b>OFN_EXPLORER</b> flag is not set.

To display a dialog box that allows the user to select a directory instead of a file, call the <a href="_win32_SHBrowseForFolder">SHBrowseForFolder</a> function.

Note, when selecting multiple files, the total character limit for the file names depends on the version of the function.

<ul>
<li>ANSI: 32k limit</li>
<li>Unicode: no restriction </li>
</ul>

#### Examples

For an example, see <a href="using_common_dialog_boxes.htm">Opening a File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/424e9d85-853b-4dc6-a29a-c532a8bb23f7">GetSaveFileName</a>



<a href="https://msdn.microsoft.com/3d3a7878-1ccc-4832-9351-8f9cf6c7a601">OFNHookProc</a>



<a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a>



<a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="_win32_SHBrowseForFolder">SHBrowseForFolder</a>
 

 

