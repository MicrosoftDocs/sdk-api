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

# CATEGORYINFO_FLAGS enumeration


## -description


Provides a set of flags for use with the <a href="https://msdn.microsoft.com/6198cd31-94db-4d31-9cc9-f8b90e661809">CATEGORY_INFO</a> structure.


## -enum-fields




### -field CATINFO_NORMAL

0x00000000. Applies default properties for the category.


### -field CATINFO_COLLAPSED

0x00000001. The category should appear as collapsed


### -field CATINFO_HIDDEN

0x00000002. The category should appear as hidden.


### -field CATINFO_EXPANDED

0x00000004. The category should appear as expanded.


### -field CATINFO_NOHEADER

0x00000008. The category has no header.


### -field CATINFO_NOTCOLLAPSIBLE

0x00000010. The category cannot be collapsed.


### -field CATINFO_NOHEADERCOUNT

0x00000020. The count of items in the category should not be displayed in the header.


### -field CATINFO_SUBSETTED

0x00000040. <b>Windows 7 and later</b>. The category should appear subsetted.


### -field CATINFO_SEPARATE_IMAGES


### -field CATINFO_SHOWEMPTY



