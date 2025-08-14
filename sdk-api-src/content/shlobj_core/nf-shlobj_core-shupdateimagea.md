---
UID: NF:shlobj_core.SHUpdateImageA
title: SHUpdateImageA function (shlobj_core.h)
description: Notifies the Shell that an image in the system image list has changed. (ANSI)
helpviewer_keywords: ["SHUpdateImageA", "shlobj_core/SHUpdateImageA"]
old-location: shell\SHUpdateImage.htm
tech.root: shell
ms.assetid: 9df5860e-db65-4e43-aaf9-c1e0e33fc569
ms.date: 12/05/2018
ms.keywords: SHUpdateImage, SHUpdateImage function [Windows Shell], SHUpdateImageA, SHUpdateImageW, _win32_SHUpdateImage, shell.SHUpdateImage, shlobj_core/SHUpdateImage, shlobj_core/SHUpdateImageA, shlobj_core/SHUpdateImageW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHUpdateImageW (Unicode) and SHUpdateImageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.7 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHUpdateImageA
 - shlobj_core/SHUpdateImageA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-shell-changenotify-l1-1-1.dll
 - Shell32.dll
api_name:
 - SHUpdateImage
 - SHUpdateImageA
 - SHUpdateImageW
---

# SHUpdateImageA function


## -description

Notifies the Shell that an image in the system image list has changed.

## -parameters

### -param pszHashItem [in]

Type: <b>LPCTSTR</b>

A pointer to a string value that specifies the fully qualified path of the file that contains the icon. Use the path that is returned in the buffer pointed to by the <i>szIconFile</i> parameter of <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a>.

### -param iIndex [in]

Type: <b>int</b>

An integer that specifies the zero-based index of the icon in the file specified by <i>pszHashItem</i>. Use the value that is pointed to by the <i>piIndex</i> parameter of <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a>.

### -param uFlags [in]

Type: <b>UINT</b>

An unsigned integer that specifies the flags that determine the icon attributes. Set <i>uFlags</i> to the value that is pointed to by the <i>pwFlags</i> parameter of <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a>. The flags that are relevant to <b>SHUpdateImage</b> are <b>GIL_NOTFILENAME</b> and <b>GIL_SIMULATEDOC</b>.

### -param iImageIndex [in]

Type: <b>int</b>

An integer that specifies the index in the system image list of the icon that is being updated.

## -remarks

If you do not know the index in the system image list of the icon that you want to update, use <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a> with the <i>uFlags</i> parameter set to <b>SHGFI_SYSICONINDEX</b>.

You must use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> with the parameters of the old icon that needs to be updated, not those of the new icon you want to replace it with.





> [!NOTE]
> The shlobj_core.h header defines SHUpdateImage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a>
