---
UID: NF:commdlg.GetSaveFileNameW
title: GetSaveFileNameW function (commdlg.h)
author: windows-sdk-content
description: Creates a Save dialog box that lets the user specify the drive, directory, and name of a file to save.
old-location: dlgbox\getsavefilename.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\getsavefilename.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSaveFileName, GetSaveFileName function [Dialog Boxes], GetSaveFileNameA, GetSaveFileNameW, _win32_GetSaveFileName, _win32_getsavefilename_cpp, commdlg/GetSaveFileName, commdlg/GetSaveFileNameA, commdlg/GetSaveFileNameW, dlgbox.getsavefilename, winui._win32_getsavefilename
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

# GetSaveFileNameW function


## -description


<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="https://msdn.microsoft.com/en-us/library/Bb776913(v=VS.85).aspx">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Creates a <b>Save</b> dialog box that lets the user specify the drive, directory, and name of a file to save.


## -parameters




### -param Arg1 [in, out]

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure that contains information used to initialize the dialog box. When <b>GetSaveFileName</b> returns, this structure contains information about the user's file selection.


## -returns



Type: <b>BOOL</b>

If the user specifies a file name and clicks the 
						<b>OK</b> button and the function is successful, the return value is nonzero. The buffer pointed to by the 
						<b>lpstrFile</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure contains the full path and file name specified by the user.

If the user cancels or closes the 
						<b>Save</b> dialog box or an error such as the file name buffer being too small occurs, the return value is zero. To get extended error information, call the <a href="https://msdn.microsoft.com/en-us/library/ms646916(v=VS.85).aspx">CommDlgExtendedError</a> function, which can return one of the following values: 




## -remarks



The Explorer-style <b>Save</b> dialog box that provides user-interface features that are similar to the Windows Explorer. You can provide an <a href="https://msdn.microsoft.com/en-us/library/ms646931(v=VS.85).aspx">OFNHookProc</a> hook procedure for an Explorer-style <b>Save</b> dialog box. To enable the hook procedure, set the <b>OFN_EXPLORER</b> and <b>OFN_ENABLEHOOK</b> flags in the  <b>Flags</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure and specify the address of the hook procedure in the  <b>lpfnHook</b> member.

Windows continues to support old-style <b>Save</b> dialog boxes for applications that want to maintain a user-interface consistent with the old-style user-interface. To display the old-style <b>Save</b> dialog box, enable an <a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a> hook procedure and ensure that the <b>OFN_EXPLORER</b> flag is not set.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/084b2737-eb55-4587-b8e8-3eb3fa3688c4">Creating an Enhanced Metafile</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646916(v=VS.85).aspx">CommDlgExtendedError</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646927(v=VS.85).aspx">GetOpenFileName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646931(v=VS.85).aspx">OFNHookProc</a>



<a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a>



<b>Reference</b>
 

 

