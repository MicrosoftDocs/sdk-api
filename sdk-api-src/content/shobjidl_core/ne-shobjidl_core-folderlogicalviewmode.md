---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

