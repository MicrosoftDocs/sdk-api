---
UID: NF:winuser.DlgDirSelectExA
title: DlgDirSelectExA function (winuser.h)
description: Retrieves the current selection from a single-selection list box. It assumes that the list box has been filled by the DlgDirList function and that the selection is a drive letter, filename, or directory name. (ANSI)
helpviewer_keywords: ["DlgDirSelectExA", "winuser/DlgDirSelectExA"]
old-location: controls\DlgDirSelectEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxfunctions\dlgdirselectex.htm
ms.date: 12/05/2018
ms.keywords: DlgDirSelectEx, DlgDirSelectEx function [Windows Controls], DlgDirSelectExA, DlgDirSelectExW, _win32_DlgDirSelectEx, _win32_DlgDirSelectEx_cpp, controls.DlgDirSelectEx, controls._win32_DlgDirSelectEx, winuser/DlgDirSelectEx, winuser/DlgDirSelectExA, winuser/DlgDirSelectExW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DlgDirSelectExA
 - winuser/DlgDirSelectExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-0.dll
 - User32.dll
api_name:
 - DlgDirSelectEx
 - DlgDirSelectExA
 - DlgDirSelectExW
---

# DlgDirSelectExA function


## -description

Retrieves the current selection from a single-selection list box. It assumes that the list box has been filled by the <a href="/windows/desktop/api/winuser/nf-winuser-dlgdirlista">DlgDirList</a> function and that the selection is a drive letter, filename, or directory name.

## -parameters

### -param hwndDlg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the dialog box that contains the list box.

### -param lpString [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the current selection is a directory name, the return value is nonzero.

If the current selection is not a directory name, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>DlgDirSelectEx</b> function copies the selection to the buffer pointed to by the 
                <i>lpString</i> parameter. If the current selection is a directory name or drive letter, <b>DlgDirSelectEx</b> removes the enclosing square brackets (and hyphens, for drive letters), so that the name or letter is ready to be inserted into a new path. If there is no selection, 
                <i>lpString</i> does not change.

If the string is as long or longer than the buffer, the buffer will contain the truncated string with a terminating null character.

<b>DlgDirSelectEx</b> sends <a href="/windows/desktop/Controls/lb-getcursel">LB_GETCURSEL</a> and <a href="/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a> messages to the list box. The function does not allow more than one filename to be returned from a list box. The list box must not be a multiple-selection list box. If it is, this function does not return a zero value and 
                <i>lpString</i> remains unchanged. 

<b>Windows 95 or later</b>: <b>DlgDirSelectExW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="/archive/msdn-magazine/2001/october/mslu-develop-unicode-applications-for-windows-9x-platforms-with-the-microsoft-layer-for-unicode">Microsoft Layer for Unicode on Windows Me/98/95 Systems</a>.


#### Examples

For an example, see <a href="/windows/desktop/Controls/using-list-boxes">Creating a Directory Listing in a Single-selection List Box</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines DlgDirSelectEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirlista">DlgDirList</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirlistcomboboxa">DlgDirListComboBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirselectcomboboxexa">DlgDirSelectComboBoxEx</a>



<a href="/windows/desktop/Controls/lb-getcursel">LB_GETCURSEL</a>



<a href="/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a>



<b>Reference</b>
