---
UID: NE:shobjidl_core.FOLDERVIEWMODE
title: FOLDERVIEWMODE (shobjidl_core.h)
description: Specifies the folder view type.
helpviewer_keywords: ["FOLDERVIEWMODE","FOLDERVIEWMODE enumeration [Windows Shell]","FVM_AUTO","FVM_CONTENT","FVM_DETAILS","FVM_FIRST","FVM_ICON","FVM_LAST","FVM_LIST","FVM_SMALLICON","FVM_THUMBNAIL","FVM_THUMBSTRIP","FVM_TILE","_win32_FOLDERVIEWMODE","shell.FOLDERVIEWMODE","shobjidl_core/FOLDERVIEWMODE","shobjidl_core/FVM_AUTO","shobjidl_core/FVM_CONTENT","shobjidl_core/FVM_DETAILS","shobjidl_core/FVM_FIRST","shobjidl_core/FVM_ICON","shobjidl_core/FVM_LAST","shobjidl_core/FVM_LIST","shobjidl_core/FVM_SMALLICON","shobjidl_core/FVM_THUMBNAIL","shobjidl_core/FVM_THUMBSTRIP","shobjidl_core/FVM_TILE"]
old-location: shell\FOLDERVIEWMODE.htm
tech.root: shell
ms.assetid: 16b92115-6e7d-41d3-960d-6783d779224c
ms.date: 12/05/2018
ms.keywords: FOLDERVIEWMODE, FOLDERVIEWMODE enumeration [Windows Shell], FVM_AUTO, FVM_CONTENT, FVM_DETAILS, FVM_FIRST, FVM_ICON, FVM_LAST, FVM_LIST, FVM_SMALLICON, FVM_THUMBNAIL, FVM_THUMBSTRIP, FVM_TILE, _win32_FOLDERVIEWMODE, shell.FOLDERVIEWMODE, shobjidl_core/FOLDERVIEWMODE, shobjidl_core/FVM_AUTO, shobjidl_core/FVM_CONTENT, shobjidl_core/FVM_DETAILS, shobjidl_core/FVM_FIRST, shobjidl_core/FVM_ICON, shobjidl_core/FVM_LAST, shobjidl_core/FVM_LIST, shobjidl_core/FVM_SMALLICON, shobjidl_core/FVM_THUMBNAIL, shobjidl_core/FVM_THUMBSTRIP, shobjidl_core/FVM_TILE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FOLDERVIEWMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FOLDERVIEWMODE
 - shobjidl_core/FOLDERVIEWMODE
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
 - FOLDERVIEWMODE
---

# FOLDERVIEWMODE enumeration


## -description

Specifies the folder view type.

## -enum-fields

### -field FVM_AUTO

The view should determine the best option.

### -field FVM_FIRST

The minimum constant value in <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a>, for validation purposes.

### -field FVM_ICON

The view should display medium-size icons.

### -field FVM_SMALLICON

The view should display small icons.

### -field FVM_LIST

Object names are displayed in a list view.

### -field FVM_DETAILS

Object names and other selected information, such as the size or date last updated, are shown.

### -field FVM_THUMBNAIL

The view should display thumbnail icons.

### -field FVM_TILE

The view should display large icons.

### -field FVM_THUMBSTRIP

The view should display icons in a filmstrip format.

### -field FVM_CONTENT

<b>Windows 7 and later</b>. The view should display content mode.

### -field FVM_LAST

The maximum constant value in <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a>, for validation purposes.