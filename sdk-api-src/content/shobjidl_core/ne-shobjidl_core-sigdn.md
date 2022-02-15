---
UID: NE:shobjidl_core._SIGDN
title: SIGDN (shobjidl_core.h)
description: Requests the form of an item's display name to retrieve through IShellItem::GetDisplayName and SHGetNameFromIDList.
helpviewer_keywords: ["SIGDN","SIGDN enumeration [Windows Shell]","SIGDN_DESKTOPABSOLUTEEDITING","SIGDN_DESKTOPABSOLUTEPARSING","SIGDN_FILESYSPATH","SIGDN_NORMALDISPLAY","SIGDN_PARENTRELATIVE","SIGDN_PARENTRELATIVEEDITING","SIGDN_PARENTRELATIVEFORADDRESSBAR","SIGDN_PARENTRELATIVEFORUI","SIGDN_PARENTRELATIVEPARSING","SIGDN_URL","inet_SIGDN","shell.SIGDN","shobjidl_core/SIGDN","shobjidl_core/SIGDN_DESKTOPABSOLUTEEDITING","shobjidl_core/SIGDN_DESKTOPABSOLUTEPARSING","shobjidl_core/SIGDN_FILESYSPATH","shobjidl_core/SIGDN_NORMALDISPLAY","shobjidl_core/SIGDN_PARENTRELATIVE","shobjidl_core/SIGDN_PARENTRELATIVEEDITING","shobjidl_core/SIGDN_PARENTRELATIVEFORADDRESSBAR","shobjidl_core/SIGDN_PARENTRELATIVEFORUI","shobjidl_core/SIGDN_PARENTRELATIVEPARSING","shobjidl_core/SIGDN_URL"]
old-location: shell\SIGDN.htm
tech.root: shell
ms.assetid: ef800ed8-8694-4543-ad33-c81b976cc5c2
ms.date: 12/05/2018
ms.keywords: SIGDN, SIGDN enumeration [Windows Shell], SIGDN_DESKTOPABSOLUTEEDITING, SIGDN_DESKTOPABSOLUTEPARSING, SIGDN_FILESYSPATH, SIGDN_NORMALDISPLAY, SIGDN_PARENTRELATIVE, SIGDN_PARENTRELATIVEEDITING, SIGDN_PARENTRELATIVEFORADDRESSBAR, SIGDN_PARENTRELATIVEFORUI, SIGDN_PARENTRELATIVEPARSING, SIGDN_URL, inet_SIGDN, shell.SIGDN, shobjidl_core/SIGDN, shobjidl_core/SIGDN_DESKTOPABSOLUTEEDITING, shobjidl_core/SIGDN_DESKTOPABSOLUTEPARSING, shobjidl_core/SIGDN_FILESYSPATH, shobjidl_core/SIGDN_NORMALDISPLAY, shobjidl_core/SIGDN_PARENTRELATIVE, shobjidl_core/SIGDN_PARENTRELATIVEEDITING, shobjidl_core/SIGDN_PARENTRELATIVEFORADDRESSBAR, shobjidl_core/SIGDN_PARENTRELATIVEFORUI, shobjidl_core/SIGDN_PARENTRELATIVEPARSING, shobjidl_core/SIGDN_URL
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SIGDN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SIGDN
 - shobjidl_core/_SIGDN
 - SIGDN
 - shobjidl_core/SIGDN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SIGDN
---

# SIGDN enumeration


## -description

Requests the form of an item's display name to retrieve through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname">IShellItem::GetDisplayName</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist">SHGetNameFromIDList</a>.

## -enum-fields

### -field SIGDN_NORMALDISPLAY:0

0x00000000. Returns the display name relative to the parent folder. In UI this name is generally ideal for display to the user.

### -field SIGDN_PARENTRELATIVEPARSING

(int)0x80018001. Returns the parsing name relative to the parent folder. This name is not suitable for use in UI.

### -field SIGDN_DESKTOPABSOLUTEPARSING

(int)0x80028000. Returns the parsing name relative to the desktop. This name is not suitable for use in UI.

### -field SIGDN_PARENTRELATIVEEDITING

(int)0x80031001. Returns the editing name relative to the parent folder. In UI this name is suitable for display to the user.

### -field SIGDN_DESKTOPABSOLUTEEDITING

(int)0x8004c000. Returns the editing name relative to the desktop. In UI this name is suitable for display to the user.

### -field SIGDN_FILESYSPATH

(int)0x80058000. Returns the item's file system path, if it has one. Only items that report <a href="/windows/desktop/shell/sfgao">SFGAO_FILESYSTEM</a> have a file system path. When an item does not have a file system path, a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname">IShellItem::GetDisplayName</a> on that item will fail. In UI this name is suitable for display to the user in some cases, but note that it might not be specified for all items.

### -field SIGDN_URL

(int)0x80068000. Returns the item's URL, if it has one. Some items do not have a URL, and in those cases a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname">IShellItem::GetDisplayName</a> will fail. This name is suitable for display to the user in some cases, but note that it might not be specified for all items.

### -field SIGDN_PARENTRELATIVEFORADDRESSBAR

(int)0x8007c001. Returns the path relative to the parent folder in a friendly format as displayed in an address bar. This name is suitable for display to the user.

### -field SIGDN_PARENTRELATIVE

(int)0x80080001. Returns the path relative to the parent folder.

### -field SIGDN_PARENTRELATIVEFORUI

(int)0x80094001. <b>Introduced in Windows 8</b>.

## -remarks

Different forms of an item's name can be retrieved through the item's properties, including those listed here. Note that not all properties are present on all items, so only those appropriate to the item will appear.
            
                

<ul>
<li>
<a href="/windows/desktop/properties/props-system-filename">PKEY_FileName</a>
</li>
<li>
<a href="/windows/desktop/properties/props-system-itemfoldernamedisplay">PKEY_ItemFolderNameDisplay</a>
</li>
<li>
<a href="/windows/desktop/properties/props-system-itemfolderpathdisplay">PKEY_ItemFolderPathDisplay</a>
</li>
<li>
<a href="/windows/desktop/properties/props-system-itemfolderpathdisplaynarrow">PKEY_ItemFolderPathDisplayNarrow</a>
</li>
</ul>
