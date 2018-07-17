---
UID: NF:shlobj_core.SHGetIconOverlayIndexW
title: SHGetIconOverlayIndexW function
author: windows-sdk-content
description: Returns the index of the overlay icon in the system image list.
old-location: shell\SHGetIconOverlayIndex.htm
old-project: shell
ms.assetid: 20001ae0-05d0-46a7-8bb8-9bb722f5d795
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IDO_SHGIOI_DEFAULT, IDO_SHGIOI_LINK, IDO_SHGIOI_SHARE, IDO_SHGIOI_SLOWFILE, SHGetIconOverlayIndex, SHGetIconOverlayIndex function [Windows Shell], SHGetIconOverlayIndexA, SHGetIconOverlayIndexW, _win32_SHGetIconOverlayIndex, shell.SHGetIconOverlayIndex, shlobj_core/SHGetIconOverlayIndex, shlobj_core/SHGetIconOverlayIndexA, shlobj_core/SHGetIconOverlayIndexW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
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
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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



Icon overlays are part of the system image list. They have two identifiers. The first is a one-based overlay index that identifies the overlay relative to other overlays in the image list. The other is an image index that identifies the actual image. These two indexes are equivalent to the values that you assign to the <i>iOverlay</i> and <i>iImage</i> parameters, respectively, when you add an icon overlay to a private image list with <a href="https://msdn.microsoft.com/library/Bb775227(v=VS.85).aspx">ImageList_SetOverlayImage</a>. <b>SHGetIconOverlayIndex</b> returns the overlay index. To convert an overlay index to its equivalent image index, call <a href="https://msdn.microsoft.com/library/Bb761408(v=VS.85).aspx">INDEXTOOVERLAYMASK</a>.

<div class="alert"><b>Note</b>  After the image has been loaded into the system image list during initialization, it cannot be changed. The file name and index specified by <i>pszIconPath</i> and <i>iIconIndex</i> are used only to identify the icon overlay. <b>SHGetIconOverlayIndex</b> cannot be used to modify the system image list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1a1d03ca-0922-41df-8cec-e74a16ed3bd6">IShellIconOverlay</a>



<a href="https://msdn.microsoft.com/c093bc13-def7-411d-b741-50996ffad84b">IShellIconOverlayIdentifier</a>
 

 

