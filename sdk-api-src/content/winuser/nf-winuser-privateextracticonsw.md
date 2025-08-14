---
UID: NF:winuser.PrivateExtractIconsW
title: PrivateExtractIconsW function (winuser.h)
description: Creates an array of handles to icons that are extracted from a specified file. (Unicode)
helpviewer_keywords: ["PrivateExtractIcons", "PrivateExtractIcons function [Menus and Other Resources]", "PrivateExtractIconsW", "_win32_PrivateExtractIcons", "_win32_privateextracticons_cpp", "menurc.privateextracticons", "winui._win32_privateextracticons", "winuser/PrivateExtractIcons", "winuser/PrivateExtractIconsW"]
old-location: menurc\privateextracticons.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\privateextracticons.htm
ms.date: 12/05/2018
ms.keywords: PrivateExtractIcons, PrivateExtractIcons function [Menus and Other Resources], PrivateExtractIconsA, PrivateExtractIconsW, _win32_PrivateExtractIcons, _win32_privateextracticons_cpp, menurc.privateextracticons, winui._win32_privateextracticons, winuser/PrivateExtractIcons, winuser/PrivateExtractIconsA, winuser/PrivateExtractIconsW
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PrivateExtractIconsW (Unicode) and PrivateExtractIconsA (ANSI)
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
 - PrivateExtractIconsW
 - winuser/PrivateExtractIconsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - PrivateExtractIcons
 - PrivateExtractIconsA
 - PrivateExtractIconsW
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# PrivateExtractIconsW function


## -description

<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Creates an array of handles to icons that are extracted from a specified file.

## -parameters

### -param szFileName [in]

Type: <b>LPCTSTR</b>

The path and name of the file
				from which the icon(s) are to be extracted.

### -param nIconIndex [in]

Type: <b>int</b>

The zero-based index of the first icon to extract. For example,
				  if this value is zero, the function extracts the first icon in the specified
				  file.

### -param cxIcon [in]

Type: <b>int</b>

The horizontal icon size wanted. See Remarks.

### -param cyIcon [in]

Type: <b>int</b>

The vertical icon size wanted. See Remarks.

### -param phicon [out, optional]

Type: <b>HICON*</b>

A pointer to the returned array of icon handles.

### -param piconid [out, optional]

Type: <b>UINT*</b>

A pointer to a returned resource identifier for the icon that best
				fits the current display device.  The returned identifier is 0xFFFFFFFF if the
				identifier is not available for this format.  The returned identifier is 0 if
				the identifier cannot otherwise be obtained.

### -param nIcons [in]

Type: <b>UINT</b>

The number of icons to extract from the file. This parameter
				is only valid when extracting from .exe and .dll files.

### -param flags [in]

Type: <b>UINT</b>

Specifies flags that control this function.  These flags are the LR_*
				flags used by the <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> function.

## -returns

Type: <b>UINT</b>

If the <i>phicon</i> parameter is <b>NULL</b> and this function succeeds, then the return
				value is the number of icons in the file.  If the function fails then the
				return value is 0.

If the <i>phicon</i> parameter is
        not <b>NULL</b> and the function succeeds, then the return value is the
        number of icons extracted.  Otherwise, the return value is 0xFFFFFFFF if the file
        is not found.

## -remarks

This function extracts from executable (.exe), DLL (.dll),
      icon (.ico), cursor (.cur), animated cursor (.ani), and bitmap (.bmp) files.
      Extractions from Windows 3.x 16-bit executables (.exe or .dll) are
      also supported.

The <i>cxIcon</i> and
      <i>cyIcon</i> parameters specify the
      size of the icons to extract.  Two sizes can be extracted by putting the
      first size in the LOWORD of the parameter and the second size in the HIWORD.
      For example, <code>MAKELONG(24, 48)</code> for both the cxIcon and cyIcon parameters would extract
      both 24 and 48 size icons.

You must destroy all icons extracted by <b>PrivateExtractIcons</b> by calling the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function. 

This function was not included in the SDK headers and libraries until Windows XP Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.





> [!NOTE]
> The winuser.h header defines PrivateExtractIcons as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<b>Reference</b>
