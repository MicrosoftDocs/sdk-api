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

# _ads_attr_def structure


## -description


The <b>ADS_ATTR_DEF</b> structure is used only as a part of <b>IDirectorySchemaMgmt</b>, which is an obsolete interface.  The following information is provided for legacy purposes only.
   

The <b>ADS_ATTR_DEF</b> structure describes schema data for an attribute. It is used to manage attribute definitions in the schema.


## -struct-fields




### -field pszAttrName

The null-terminated Unicode string that contains the name of the attribute.


### -field dwADsType

Data type of the attribute as defined by  <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>.


### -field dwMinRange

Minimum legal range for this attribute.


### -field dwMaxRange

Maximum legal range for this attribute.


### -field fMultiValued

Whether or not this attribute takes more than one value.


## -remarks



In ADSI, attributes and properties are used interchangeably.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>
 

 

