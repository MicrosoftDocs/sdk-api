---
UID: NF:winuser.DlgDirSelectComboBoxExW
title: DlgDirSelectComboBoxExW function (winuser.h)
description: Retrieves the current selection from a combo box filled by using the DlgDirListComboBox function. The selection is interpreted as a drive letter, a file, or a directory name.
helpviewer_keywords: ["DlgDirSelectComboBoxEx","DlgDirSelectComboBoxEx function [Windows Controls]","DlgDirSelectComboBoxExA","DlgDirSelectComboBoxExW","_win32_DlgDirSelectComboBoxEx","_win32_DlgDirSelectComboBoxEx_cpp","controls.DlgDirSelectComboBoxEx","controls._win32_DlgDirSelectComboBoxEx","winuser/DlgDirSelectComboBoxEx","winuser/DlgDirSelectComboBoxExA","winuser/DlgDirSelectComboBoxExW"]
old-location: controls\DlgDirSelectComboBoxEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxfunctions\dlgdirselectcomboboxex.htm
ms.date: 12/05/2018
ms.keywords: DlgDirSelectComboBoxEx, DlgDirSelectComboBoxEx function [Windows Controls], DlgDirSelectComboBoxExA, DlgDirSelectComboBoxExW, _win32_DlgDirSelectComboBoxEx, _win32_DlgDirSelectComboBoxEx_cpp, controls.DlgDirSelectComboBoxEx, controls._win32_DlgDirSelectComboBoxEx, winuser/DlgDirSelectComboBoxEx, winuser/DlgDirSelectComboBoxExA, winuser/DlgDirSelectComboBoxExW
f1_keywords:
- winuser/DlgDirSelectComboBoxEx
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DlgDirSelectComboBoxExW (Unicode) and DlgDirSelectComboBoxExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
api_name:
- DlgDirSelectComboBoxEx
- DlgDirSelectComboBoxExA
- DlgDirSelectComboBoxExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DlgDirSelectComboBoxExW function


## -description


Retrieves the current selection from a combo box filled by using the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-dlgdirlistcomboboxa">DlgDirListComboBox</a> function. The selection is interpreted as a drive letter, a file, or a directory name. 


## -parameters




### -param hwndDlg [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the dialog box that contains the combo box. 


### -param lpString [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to the buffer that receives the selected path. 


### -param cchOut [in]

Type: <b>int</b>

The length, in characters, of the buffer pointed to by the <i>lpString</i> parameter. 


### -param idComboBox [in]

Type: <b>int</b>

The integer identifier of the combo box control in the dialog box. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the current selection is a directory name, the return value is nonzero.
                
                    

If the current selection is not a directory name, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



If the current selection specifies a directory name or drive letter, the <b>DlgDirSelectComboBoxEx</b> function removes the enclosing square brackets (and hyphens for drive letters) so the name or letter is ready to be inserted into a new path or file name. If there is no selection, the contents of the buffer pointed to by <i>lpString</i> do not change.

The <b>DlgDirSelectComboBoxEx</b> function does not allow more than one file name to be returned from a combo box. 

If the string is as long or longer than the buffer, the buffer contains the truncated string with a terminating null character.

<b>DlgDirSelectComboBoxEx</b> sends <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getcursel">CB_GETCURSEL</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a> messages to the combo box. 

You can use this function with all three types of combo boxes (<a href="https://docs.microsoft.com/windows/desktop/Controls/combo-box-styles">CBS_SIMPLE</a>, <a href="https://docs.microsoft.com/windows/desktop/Controls/combo-box-styles">CBS_DROPDOWN</a>, and CBS_DROPDOWNLIST). 

<b>Security Warning:  </b>Improper use of this function can cause problems for your application. For instance, the <i>nCount</i> parameter should be set properly for both ANSI and Unicode versions. Failure to do so could lead to a buffer overflow. You should review <a href="https://docs.microsoft.com/windows/desktop/Controls/sec-comctls">Security Considerations: Microsoft Windows Controls</a> before continuing.

<b>Windows 95 or later</b>: <b>DlgDirSelectComboBoxExW</b> is supported by the Microsoft Layer for Unicode (MSLU). To use this, you must add certain files to your application, as outlined in <a href="https://www.microsoft.com/en-us/download/details.aspx?id=4237">Microsoft Layer for Unicode on Windows Me/98/95 Systems</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getcursel">CB_GETCURSEL</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-dlgdirlistcomboboxa">DlgDirListComboBox</a>



<b>Reference</b>
 

 

