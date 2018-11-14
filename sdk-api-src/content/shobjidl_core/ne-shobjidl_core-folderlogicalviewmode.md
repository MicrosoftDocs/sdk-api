---
UID: NE:shobjidl_core.FOLDERLOGICALVIEWMODE
title: FOLDERLOGICALVIEWMODE
author: windows-sdk-content
description: Used by IFolderViewSettings::GetViewMode and ISearchFolderItemFactory::SetFolderLogicalViewMode to describe the view mode.
old-location: shell\FOLDERLOGICALVIEWMODE.htm
tech.root: shell
ms.assetid: 4b30a335-ed80-4774-82d4-bc93c95ee80c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FLVM_CONTENT, FLVM_DETAILS, FLVM_FIRST, FLVM_ICONS, FLVM_LAST, FLVM_LIST, FLVM_TILES, FLVM_UNSPECIFIED, FOLDERLOGICALVIEWMODE, FOLDERLOGICALVIEWMODE enumeration [Windows Shell], _shell_FOLDERLOGICALVIEWMODE, shell.FOLDERLOGICALVIEWMODE, shobjidl_core/FLVM_CONTENT, shobjidl_core/FLVM_DETAILS, shobjidl_core/FLVM_FIRST, shobjidl_core/FLVM_ICONS, shobjidl_core/FLVM_LAST, shobjidl_core/FLVM_LIST, shobjidl_core/FLVM_TILES, shobjidl_core/FLVM_UNSPECIFIED, shobjidl_core/FOLDERLOGICALVIEWMODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FOLDERLOGICALVIEWMODE
product: Windows
targetos: Windows
req.typenames: FOLDERLOGICALVIEWMODE
req.redist: 
---

# FOLDERLOGICALVIEWMODE enumeration


## -description


Used by <a href="https://msdn.microsoft.com/4b050a69-39df-41f8-8d54-8c576bad3c2d">IFolderViewSettings::GetViewMode</a> and <a href="https://msdn.microsoft.com/ef72f196-cfd5-4547-85cb-0ccfdc496c46">ISearchFolderItemFactory::SetFolderLogicalViewMode</a> to describe the view mode.


## -enum-fields




### -field FLVM_UNSPECIFIED

The view is not specified.


### -field FLVM_FIRST

The minimum valid enumeration value. Used for validation purposes only.


### -field FLVM_DETAILS

Details view.


### -field FLVM_TILES

Tiles view.


### -field FLVM_ICONS

Icons view.


### -field FLVM_LIST

<b>Windows 7 and later</b>. List view.


### -field FLVM_CONTENT

<b>Windows 7 and later</b>. Content view.


### -field FLVM_LAST

The maximum valid enumeration value. Used for validation purposes only.

