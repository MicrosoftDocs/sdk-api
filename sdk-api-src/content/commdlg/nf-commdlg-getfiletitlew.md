---
UID: NF:commdlg.GetFileTitleW
title: GetFileTitleW function (commdlg.h)
description: Retrieves the name of the specified file. (Unicode)
helpviewer_keywords: ["GetFileTitle", "GetFileTitle function [Dialog Boxes]", "GetFileTitleW", "_win32_GetFileTitle", "_win32_getfiletitle_cpp", "commdlg/GetFileTitle", "commdlg/GetFileTitleW", "dlgbox.getfiletitle", "winui._win32_getfiletitle"]
old-location: dlgbox\getfiletitle.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\getfiletitle.htm
ms.date: 12/05/2018
ms.keywords: GetFileTitle, GetFileTitle function [Dialog Boxes], GetFileTitleA, GetFileTitleW, _win32_GetFileTitle, _win32_getfiletitle_cpp, commdlg/GetFileTitle, commdlg/GetFileTitleA, commdlg/GetFileTitleW, dlgbox.getfiletitle, winui._win32_getfiletitle
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileTitleW (Unicode) and GetFileTitleA (ANSI)
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
 - GetFileTitleW
 - commdlg/GetFileTitleW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comdlg32.dll
 - ext-ms-win-shell-comdlg32-l1-1-1.dll
api_name:
 - GetFileTitle
 - GetFileTitleA
 - GetFileTitleW
req.apiset: ext-ms-win-shell-comdlg32-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# GetFileTitleW function


## -description

Retrieves the name of the specified file.

## -parameters

### -param unnamedParam1 [in]

Type: <b>LPCTSTR</b>

The name and location of a file.

### -param Buf [out]

Type: <b>LPTSTR</b>

The buffer that receives the name of the file.

### -param cchSize [in]

Type: <b>WORD</b>

The length, in 
					characters, of the buffer pointed to by the <i>lpszTitle</i> parameter.

## -returns

Type: <b>short</b>

If the function succeeds, the return value is zero.

If the file name is invalid, the return value is unknown. If there is an error, the return value is a negative number.

If the buffer pointed to by the <i>lpszTitle</i> parameter is too small, the return value is a positive integer that specifies the required buffer size, in characters. The required buffer size includes the terminating null character.

## -remarks

<b>GetFileTitle</b> should only be called with legal file names; using an illegal file name has an undefined result.

To get the buffer size needed for the name of a file, call the function with  <i>lpszTitle</i> set to <b>NULL</b> and  <i>cchSize</i> set to zero. The function returns the required size.

<b>GetFileTitle</b> returns the string that the system would use to display the file name to the user. The display name includes an extension only if that is the user's preference for displaying file names. This means that the returned string may not accurately identify the file if it is used in calls to file system functions.

If the  <i>lpszTitle</i> buffer is too small, <b>GetFileTitle</b> returns the size required to hold the display name. However, there is no guaranteed relationship between the required size and the characters originally specified in the  <i>lpszFile</i> buffer. For example, do not call <b>GetFileTitle</b> with  <i>lpszTitle</i> set to <b>NULL</b> and  <i>cchSize</i> set to zero, and then try to use the return value as an index into the  <i>lpszFile</i> string. You can usually achieve similar results (and superior performance) with C run-time library functions such as <b>strrchr</b>, <b>wcsrchr</b>, and <b>_mbsrchr</b>.





> [!NOTE]
> The commdlg.h header defines GetFileTitle as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a>



<b>Reference</b>
