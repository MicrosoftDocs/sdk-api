---
UID: NF:commdlg.GetSaveFileNameA
title: GetSaveFileNameA function
author: windows-sdk-content
description: Creates a Save dialog box that lets the user specify the drive, directory, and name of a file to save.
old-location: dlgbox\getsavefilename.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\getsavefilename.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSaveFileName, GetSaveFileName function [Dialog Boxes], GetSaveFileNameA, GetSaveFileNameW, _win32_GetSaveFileName, _win32_getsavefilename_cpp, commdlg/GetSaveFileName, commdlg/GetSaveFileNameA, commdlg/GetSaveFileNameW, dlgbox.getsavefilename, winui._win32_getsavefilename
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
req.unicode-ansi: GetSaveFileNameW (Unicode) and GetSaveFileNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UDACCEL, *LPUDACCEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comdlg32.dll
 - ext-ms-win-shell-comdlg32-l1-1-0.dll
api_name:
 - GetSaveFileName
 - GetSaveFileNameA
 - GetSaveFileNameW
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll
req.irql: 
---

# GetSaveFileNameA function


## -description


<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="_shell_common_file_dialog">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Creates a <b>Save</b> dialog box that lets the user specify the drive, directory, and name of a file to save.


## -parameters




### -param Arg1 [in, out]

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure that contains information used to initialize the dialog box. When <b>GetSaveFileName</b> returns, this structure contains information about the user's file selection.


## -returns



Type: <b>BOOL</b>

If the user specifies a file name and clicks the 
						<b>OK</b> button and the function is successful, the return value is nonzero. The buffer pointed to by the 
						<b>lpstrFile</b> member of the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure contains the full path and file name specified by the user.

If the user cancels or closes the 
						<b>Save</b> dialog box or an error such as the file name buffer being too small occurs, the return value is zero. To get extended error information, call the <a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a> function, which can return one of the following values: 




## -remarks



The Explorer-style <b>Save</b> dialog box that provides user-interface features that are similar to the Windows Explorer. You can provide an <a href="https://msdn.microsoft.com/3d3a7878-1ccc-4832-9351-8f9cf6c7a601">OFNHookProc</a> hook procedure for an Explorer-style <b>Save</b> dialog box. To enable the hook procedure, set the <b>OFN_EXPLORER</b> and <b>OFN_ENABLEHOOK</b> flags in the  <b>Flags</b> member of the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure and specify the address of the hook procedure in the  <b>lpfnHook</b> member.

Windows continues to support old-style <b>Save</b> dialog boxes for applications that want to maintain a user-interface consistent with the old-style user-interface. To display the old-style <b>Save</b> dialog box, enable an <a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a> hook procedure and ensure that the <b>OFN_EXPLORER</b> flag is not set.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/084b2737-eb55-4587-b8e8-3eb3fa3688c4">Creating an Enhanced Metafile</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/20c94a3d-7856-4fa1-86ef-2005b418c0bb">CommDlgExtendedError</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/22b8f3d0-455a-4eb8-9835-e90d41924ec7">GetOpenFileName</a>



<a href="https://msdn.microsoft.com/3d3a7878-1ccc-4832-9351-8f9cf6c7a601">OFNHookProc</a>



<a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a>



<a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a>



<b>Reference</b>
 

 

