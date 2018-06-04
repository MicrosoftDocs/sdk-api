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

# DEFAULT_FOLDER_MENU_RESTRICTIONS enumeration


## -description





## -enum-fields




### -field DFMR_DEFAULT

Default. 0x0000. No restrictions.


### -field DFMR_NO_STATIC_VERBS

0x0008.


### -field DFMR_STATIC_VERBS_ONLY

0x0010.


### -field DFMR_NO_RESOURCE_VERBS

0x0020.


### -field DFMR_OPTIN_HANDLERS_ONLY

0x0040.


### -field DFMR_RESOURCE_AND_FOLDER_VERBS_ONLY

0x0080.


### -field DFMR_USE_SPECIFIED_HANDLERS

0x0100.


### -field DFMR_USE_SPECIFIED_VERBS

0x0200.


### -field DFMR_NO_ASYNC_VERBS

0x0400.


### -field DFMR_NO_NATIVECPU_VERBS




## -see-also




<a href="https://msdn.microsoft.com/373240B8-E99E-4ff9-B47A-3B31B4F0B81E">IDefaultFolderMenuInitialize::GetMenuRestrictions</a>



<a href="https://msdn.microsoft.com/7D907B01-E0C4-428b-A8A4-FA383B0970BF">IDefaultFolderMenuInitialize::SetMenuRestrictions</a>
 

 

