---
UID: NF:shlobj_core.SHDefExtractIconA
title: SHDefExtractIconA function (shlobj_core.h)
description: Provides a default handler to extract an icon from a file. (ANSI)
helpviewer_keywords: ["GIL_SIMULATEDOC", "SHDefExtractIconA", "shlobj_core/SHDefExtractIconA"]
old-location: shell\SHDefExtractIcon.htm
tech.root: shell
ms.assetid: fbaa600a-5e5c-4948-81fb-d2c3993dcd47
ms.date: 12/05/2018
ms.keywords: GIL_SIMULATEDOC, SHDefExtractIcon, SHDefExtractIcon function [Windows Shell], SHDefExtractIconA, SHDefExtractIconW, _win32_SHDefExtractIcon, shell.SHDefExtractIcon, shlobj_core/SHDefExtractIcon, shlobj_core/SHDefExtractIconA, shlobj_core/SHDefExtractIconW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHDefExtractIconW (Unicode) and SHDefExtractIconA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHDefExtractIconA
 - shlobj_core/SHDefExtractIconA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHDefExtractIcon
 - SHDefExtractIconA
 - SHDefExtractIconW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHDefExtractIconA function


## -description

Provides a default handler to extract an icon from a file.

## -parameters

### -param pszIconFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated buffer that contains the path and name of the file from which the icon is extracted.

### -param iIndex

Type: <b>int</b>

The location of the icon within the file named in <i>pszIconFile</i>. If this is a positive number, it refers to the zero-based position of the icon in the file. For instance, 0 refers to the 1st icon in the resource file and 2 refers to the 3rd. If this is a negative number, it refers to the icon's resource ID.

### -param uFlags [in]

Type: <b>UINT</b>

A flag that controls the icon extraction.



#### GIL_SIMULATEDOC

Overlays the extracted icon on the default document icon to create the final icon. This icon can be used when no more appropriate icon can be found or retrieved.

### -param phiconLarge [out, optional]

Type: <b>HICON*</b>

A pointer to an HICON that, when this function returns successfully, receives the handle of the large version of the icon specified in the <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> of <i>nIconSize</i>. This value can be <b>NULL</b>.

### -param phiconSmall [out, optional]

Type: <b>HICON*</b>

A pointer to an HICON that, when this function returns successfully, receives the handle of the small version of the icon specified in the <a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a> of <i>nIconSize</i>.

### -param nIconSize

Type: <b>UINT</b>

A value that contains the large icon size in its <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> and the small icon size in its <a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a>. Size is measured in pixels. Pass 0 to specify default large and small sizes.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested icon is not present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The file cannot be accessed, or is being accessed through a slow link.

</td>
</tr>
</table>

## -remarks

It is the responsibility of the caller to free the icon resources created through this function when they are no longer needed. This can be done through the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function.




> [!NOTE]
> The shlobj_core.h header defines SHDefExtractIcon as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
