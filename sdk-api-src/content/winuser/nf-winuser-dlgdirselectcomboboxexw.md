---
UID: NF:winuser.DlgDirSelectComboBoxExW
title: DlgDirSelectComboBoxExW function
author: windows-sdk-content
description: Retrieves the current selection from a combo box filled by using the DlgDirListComboBox function. The selection is interpreted as a drive letter, a file, or a directory name.
old-location: controls\DlgDirSelectComboBoxEx.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxfunctions\dlgdirselectcomboboxex.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DlgDirSelectComboBoxEx, DlgDirSelectComboBoxEx function [Windows Controls], DlgDirSelectComboBoxExA, DlgDirSelectComboBoxExW, _win32_DlgDirSelectComboBoxEx, _win32_DlgDirSelectComboBoxEx_cpp, controls.DlgDirSelectComboBoxEx, controls._win32_DlgDirSelectComboBoxEx, winuser/DlgDirSelectComboBoxEx, winuser/DlgDirSelectComboBoxExA, winuser/DlgDirSelectComboBoxExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	DlgDirSelectComboBoxEx
-	DlgDirSelectComboBoxExA
-	DlgDirSelectComboBoxExW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DlgDirSelectComboBoxExW function


## -description


Retrieves the current selection from a combo box filled by using the <a href="https://msdn.microsoft.com/65b27196-8e85-483d-9965-e7cbc1b09b5e">DlgDirListComboBox</a> function. The selection is interpreted as a drive letter, a file, or a directory name. 


## -parameters




### -param hwndDlg

TBD


### -param lpString [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to the buffer that receives the selected path. 


### -param cchOut

TBD


### -param idComboBox

TBD




#### - hDlg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the dialog box that contains the combo box. 


#### - nCount [in]

Type: <b>int</b>

The length, in characters, of the buffer pointed to by the <i>lpString</i> parameter. 


#### - nIDComboBox [in]

Type: <b>int</b>

The integer identifier of the combo box control in the dialog box. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the current selection is a directory name, the return value is nonzero.
                
                    

If the current selection is not a directory name, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the current selection specifies a directory name or drive letter, the <b>DlgDirSelectComboBoxEx</b> function removes the enclosing square brackets (and hyphens for drive letters) so the name or letter is ready to be inserted into a new path or file name. If there is no selection, the contents of the buffer pointed to by <i>lpString</i> do not change.

The <b>DlgDirSelectComboBoxEx</b> function does not allow more than one file name to be returned from a combo box. 

If the string is as long or longer than the buffer, the buffer contains the truncated string with a terminating null character.

<b>DlgDirSelectComboBoxEx</b> sends <a href="https://msdn.microsoft.com/47bf87f6-637f-48e9-849e-b2acbe5a6a7b">CB_GETCURSEL</a> and <a href="https://msdn.microsoft.com/f84e302a-65bb-45c8-958b-1cb438fb5a7a">CB_GETLBTEXT</a> messages to the combo box. 

You can use this function with all three types of combo boxes (<a href="Combo_Box_Styles.htm">CBS_SIMPLE</a>, <a href="Combo_Box_Styles.htm">CBS_DROPDOWN</a>, and CBS_DROPDOWNLIST). 

<b>Security Warning:  </b>Improper use of this function can cause problems for your application. For instance, the <i>nCount</i> parameter should be set properly for both ANSI and Unicode versions. Failure to do so could lead to a buffer overflow. You should review <a href="https://msdn.microsoft.com/d5396fa1-452e-40e1-beaf-ae04690048f1">Security Considerations: Microsoft Windows Controls</a> before continuing.

<b>Windows 95 or later</b>: <b>DlgDirSelectComboBoxExW</b> is supported by the Microsoft Layer for Unicode (MSLU). To use this, you must add certain files to your application, as outlined in <a href=" http://go.microsoft.com/fwlink/p/?linkid=198351">Microsoft Layer for Unicode on Windows Me/98/95 Systems</a>.




## -see-also




<a href="https://msdn.microsoft.com/47bf87f6-637f-48e9-849e-b2acbe5a6a7b">CB_GETCURSEL</a>



<a href="https://msdn.microsoft.com/f84e302a-65bb-45c8-958b-1cb438fb5a7a">CB_GETLBTEXT</a>



<a href="https://msdn.microsoft.com/65b27196-8e85-483d-9965-e7cbc1b09b5e">DlgDirListComboBox</a>



<b>Reference</b>
 

 

