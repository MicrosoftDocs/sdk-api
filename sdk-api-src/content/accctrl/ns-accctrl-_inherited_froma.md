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

# _INHERITED_FROMA structure


## -description


The <b>INHERITED_FROM</b> structure provides information about an object's inherited <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE).


## -struct-fields




### -field GenerationGap

Number of levels, or generations, between the object and the ancestor. Set this to zero for an explicit ACE. If the ancestor cannot be determined for the inherited ACE, set this member to –1.


### -field AncestorName

Name of the ancestor from which the ACE was inherited. For an explicit ACE, set this to <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/c9c58b9a-1b65-40e2-b518-30e247f9718e">FreeInheritedFromArray</a>



<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>
 

 

