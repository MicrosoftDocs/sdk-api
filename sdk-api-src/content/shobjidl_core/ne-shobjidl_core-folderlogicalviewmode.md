---
UID: NE:shobjidl_core.FOLDERLOGICALVIEWMODE
title: FOLDERLOGICALVIEWMODE (shobjidl_core.h)
description: Used by IFolderViewSettings::GetViewMode and ISearchFolderItemFactory::SetFolderLogicalViewMode to describe the view mode.
helpviewer_keywords: ["FLVM_CONTENT","FLVM_DETAILS","FLVM_FIRST","FLVM_ICONS","FLVM_LAST","FLVM_LIST","FLVM_TILES","FLVM_UNSPECIFIED","FOLDERLOGICALVIEWMODE","FOLDERLOGICALVIEWMODE enumeration [Windows Shell]","_shell_FOLDERLOGICALVIEWMODE","shell.FOLDERLOGICALVIEWMODE","shobjidl_core/FLVM_CONTENT","shobjidl_core/FLVM_DETAILS","shobjidl_core/FLVM_FIRST","shobjidl_core/FLVM_ICONS","shobjidl_core/FLVM_LAST","shobjidl_core/FLVM_LIST","shobjidl_core/FLVM_TILES","shobjidl_core/FLVM_UNSPECIFIED","shobjidl_core/FOLDERLOGICALVIEWMODE"]
old-location: shell\FOLDERLOGICALVIEWMODE.htm
tech.root: shell
ms.assetid: 4b30a335-ed80-4774-82d4-bc93c95ee80c
ms.date: 12/05/2018
ms.keywords: FLVM_CONTENT, FLVM_DETAILS, FLVM_FIRST, FLVM_ICONS, FLVM_LAST, FLVM_LIST, FLVM_TILES, FLVM_UNSPECIFIED, FOLDERLOGICALVIEWMODE, FOLDERLOGICALVIEWMODE enumeration [Windows Shell], _shell_FOLDERLOGICALVIEWMODE, shell.FOLDERLOGICALVIEWMODE, shobjidl_core/FLVM_CONTENT, shobjidl_core/FLVM_DETAILS, shobjidl_core/FLVM_FIRST, shobjidl_core/FLVM_ICONS, shobjidl_core/FLVM_LAST, shobjidl_core/FLVM_LIST, shobjidl_core/FLVM_TILES, shobjidl_core/FLVM_UNSPECIFIED, shobjidl_core/FOLDERLOGICALVIEWMODE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: FOLDERLOGICALVIEWMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FOLDERLOGICALVIEWMODE
 - shobjidl_core/FOLDERLOGICALVIEWMODE
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
 - FOLDERLOGICALVIEWMODE
---

# FOLDERLOGICALVIEWMODE enumeration


## -description

Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderviewsettings-getviewmode">IFolderViewSettings::GetViewMode</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode">ISearchFolderItemFactory::SetFolderLogicalViewMode</a> to describe the view mode.

## -enum-fields

### -field FLVM_UNSPECIFIED:-1

The view is not specified.

### -field FLVM_FIRST:1

The minimum valid enumeration value. Used for validation purposes only.

### -field FLVM_DETAILS:1

Details view.

### -field FLVM_TILES:2

Tiles view.

### -field FLVM_ICONS:3

Icons view.

### -field FLVM_LIST:4

<b>Windows 7 and later</b>. List view.

### -field FLVM_CONTENT:5

<b>Windows 7 and later</b>. Content view.

### -field FLVM_LAST:5

The maximum valid enumeration value. Used for validation purposes only.
