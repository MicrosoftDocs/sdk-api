---
UID: NF:winuser.DlgDirSelectExA
title: DlgDirSelectExA function
author: windows-sdk-content
description: Retrieves the current selection from a single-selection list box. It assumes that the list box has been filled by the DlgDirList function and that the selection is a drive letter, filename, or directory name.
old-location: controls\DlgDirSelectEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxfunctions\dlgdirselectex.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: DlgDirSelectEx, DlgDirSelectEx function [Windows Controls], DlgDirSelectExA, DlgDirSelectExW, _win32_DlgDirSelectEx, _win32_DlgDirSelectEx_cpp, controls.DlgDirSelectEx, controls._win32_DlgDirSelectEx, winuser/DlgDirSelectEx, winuser/DlgDirSelectExA, winuser/DlgDirSelectExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DlgDirSelectExW (Unicode) and DlgDirSelectExA (ANSI)
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
 - DlgDirSelectEx
 - DlgDirSelectExA
 - DlgDirSelectExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DlgDirSelectExA function


## -description


Retrieves the current selection from a single-selection list box. It assumes that the list box has been filled by the <a href="https://msdn.microsoft.com/en-us/library/Bb761366(v=VS.85).aspx">DlgDirList</a> function and that the selection is a drive letter, filename, or directory name. 


## -parameters




### -param hwndDlg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the dialog box that contains the list box. 


### -param lpString [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that receives the selected path. 


### -param chCount [in]

Type: <b>int</b>

The length, in 
					<b>TCHARs</b>, of the buffer pointed to by 
					<i>lpString</i>. 


### -param idListBox [in]

Type: <b>int</b>

The identifier of a list box in the dialog box. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the current selection is a directory name, the return value is nonzero.

If the current selection is not a directory name, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>DlgDirSelectEx</b> function copies the selection to the buffer pointed to by the 
				<i>lpString</i> parameter. If the current selection is a directory name or drive letter, <b>DlgDirSelectEx</b> removes the enclosing square brackets (and hyphens, for drive letters), so that the name or letter is ready to be inserted into a new path. If there is no selection, 
				<i>lpString</i> does not change. 

If the string is as long or longer than the buffer, the buffer will contain the truncated string with a terminating null character.

<b>DlgDirSelectEx</b> sends <a href="https://msdn.microsoft.com/en-us/library/Bb775197(v=VS.85).aspx">LB_GETCURSEL</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb761313(v=VS.85).aspx">LB_GETTEXT</a> messages to the list box. The function does not allow more than one filename to be returned from a list box. The list box must not be a multiple-selection list box. If it is, this function does not return a zero value and 
				<i>lpString</i> remains unchanged. 

<b>Windows 95 or later</b>: <b>DlgDirSelectExW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href=" http://go.microsoft.com/fwlink/p/?linkid=198351">Microsoft Layer for Unicode on Windows Me/98/95 Systems</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/Bb775148(v=VS.85).aspx">Creating a Directory Listing in a Single-selection List Box</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761366(v=VS.85).aspx">DlgDirList</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775935(v=VS.85).aspx">DlgDirListComboBox</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775937(v=VS.85).aspx">DlgDirSelectComboBoxEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775197(v=VS.85).aspx">LB_GETCURSEL</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761313(v=VS.85).aspx">LB_GETTEXT</a>



<b>Reference</b>
 

 

