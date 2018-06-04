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

# __MIDL___MIDL_itf_ads_0000_0000_0008 structure


## -description


The <b>ADS_BACKLINK</b> structure is an ADSI representation of the <b>Back Link</b> attribute syntax.


## -struct-fields




### -field RemoteID

Identifier of the remote server that requires an external reference to the object specified by <b>ObjectName</b>. See below.


### -field ObjectName

The null-terminated Unicode string that specifies the name of an object to which the <b>Back Link</b> attribute is attached.


## -remarks



A <b>Back Link</b> attribute contains one or more servers that hold an external reference to the attached object.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 

