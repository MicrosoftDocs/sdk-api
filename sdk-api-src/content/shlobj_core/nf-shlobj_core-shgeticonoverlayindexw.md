---
UID: NF:shlobj_core.SHGetIconOverlayIndexW
title: SHGetIconOverlayIndexW function (shlobj_core.h)
description: Returns the index of the overlay icon in the system image list. (Unicode)
helpviewer_keywords: ["IDO_SHGIOI_DEFAULT", "IDO_SHGIOI_LINK", "IDO_SHGIOI_SHARE", "IDO_SHGIOI_SLOWFILE", "SHGetIconOverlayIndex", "SHGetIconOverlayIndex function [Windows Shell]", "SHGetIconOverlayIndexW", "_win32_SHGetIconOverlayIndex", "shell.SHGetIconOverlayIndex", "shlobj_core/SHGetIconOverlayIndex", "shlobj_core/SHGetIconOverlayIndexW"]
old-location: shell\SHGetIconOverlayIndex.htm
tech.root: shell
ms.assetid: 20001ae0-05d0-46a7-8bb8-9bb722f5d795
ms.date: 12/05/2018
ms.keywords: IDO_SHGIOI_DEFAULT, IDO_SHGIOI_LINK, IDO_SHGIOI_SHARE, IDO_SHGIOI_SLOWFILE, SHGetIconOverlayIndex, SHGetIconOverlayIndex function [Windows Shell], SHGetIconOverlayIndexA, SHGetIconOverlayIndexW, _win32_SHGetIconOverlayIndex, shell.SHGetIconOverlayIndex, shlobj_core/SHGetIconOverlayIndex, shlobj_core/SHGetIconOverlayIndexA, shlobj_core/SHGetIconOverlayIndexW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetIconOverlayIndexW (Unicode) and SHGetIconOverlayIndexA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetIconOverlayIndexW
 - shlobj_core/SHGetIconOverlayIndexW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetIconOverlayIndex
 - SHGetIconOverlayIndexA
 - SHGetIconOverlayIndexW
---

# SHGetIconOverlayIndexW function


## -description

Returns the index of the overlay icon in the system image list.

## -parameters

### -param pszIconPath [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length <b>MAX_PATH</b> that contains the fully qualified path of the file that contains the icon.

### -param iIconIndex

Type: <b>int</b>

The icon's index in the file pointed to by <i>pszIconPath</i>. To request a standard overlay icon, set <i>pszIconPath</i> to <b>NULL</b>, and <i>iIconIndex</i> to one of the following:



#### IDO_SHGIOI_SHARE (0x0FFFFFFF)

The overlay icon that indicates a shared folder.



#### IDO_SHGIOI_LINK (0x0FFFFFFE)

The overlay icon that indicates a linked folder or file.



#### IDO_SHGIOI_SLOWFILE (0x0FFFFFFD)

The overlay icon that indicates a slow file.



#### IDO_SHGIOI_DEFAULT (0x0FFFFFFC)

<b>Windows 7 and later</b>. The overlay icon that indicates that the item is the default in a set. One example is the default printer.


##### - iIconIndex.IDO_SHGIOI_DEFAULT (0x0FFFFFFC)

<b>Windows 7 and later</b>. The overlay icon that indicates that the item is the default in a set. One example is the default printer.


##### - iIconIndex.IDO_SHGIOI_LINK (0x0FFFFFFE)

The overlay icon that indicates a linked folder or file.


##### - iIconIndex.IDO_SHGIOI_SHARE (0x0FFFFFFF)

The overlay icon that indicates a shared folder.


##### - iIconIndex.IDO_SHGIOI_SLOWFILE (0x0FFFFFFD)

The overlay icon that indicates a slow file.

## -returns

Type: <b>int</b>

Returns the index of the overlay icon in the system image list if successful, or -1 otherwise.

## -remarks

Icon overlays are part of the system image list. They have two identifiers. The first is a one-based overlay index that identifies the overlay relative to other overlays in the image list. The other is an image index that identifies the actual image. These two indexes are equivalent to the values that you assign to the <i>iOverlay</i> and <i>iImage</i> parameters, respectively, when you add an icon overlay to a private image list with <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_setoverlayimage">ImageList_SetOverlayImage</a>. <b>SHGetIconOverlayIndex</b> returns the overlay index. To convert an overlay index to its equivalent image index, call <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a>.

<div class="alert"><b>Note</b>  After the image has been loaded into the system image list during initialization, it cannot be changed. The file name and index specified by <i>pszIconPath</i> and <i>iIconIndex</i> are used only to identify the icon overlay. <b>SHGetIconOverlayIndex</b> cannot be used to modify the system image list.</div>
<div> </div>




> [!NOTE]
> The shlobj_core.h header defines SHGetIconOverlayIndex as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay">IShellIconOverlay</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier">IShellIconOverlayIdentifier</a>
