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

# _tagSYNCMGRITEMFLAGS enumeration


## -description


Specifies information for the current item in the <a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a> structure.


## -enum-fields




### -field SYNCMGRITEM_HASPROPERTIES

The item has a properties dialog.


### -field SYNCMGRITEM_TEMPORARY

The item is temporary and any stored preferences can be removed. This value is defined but not used in Windows Vista.


### -field SYNCMGRITEM_ROAMINGUSER


        The item roams with the user and is not specific to a machine. This value is defined but is ignored by both Windows XP and Windows Vista.
      


### -field SYNCMGRITEM_LASTUPDATETIME

The LastUpdateTime field is valid.


### -field SYNCMGRITEM_MAYDELETEITEM


        The item may be deleted. This value has been deprecated for Windows Vista and later. This value is defined but is ignored by both Windows XP and Windows Vista.
      


### -field SYNCMGRITEM_HIDDEN

<b>Windows Vista and later</b>. Not supported.
      


## -see-also




<a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a>
 

 

