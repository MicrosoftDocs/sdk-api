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

# IMetaDataImport::GetCustomAttributeByName


## -description


Gets the custom attribute, given its name and owner.


## -parameters




### -param tkObj [in]

A metadata token representing the object that owns the custom attribute.


### -param szName [in]

The name of the custom attribute.


### -param ppData




### -param pcbData [out]

The size in bytes of the data returned in <i>const</i>.


#### - const [out]

A pointer to an array of data that is the value of the custom attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is legal to define multiple custom attributes for the same owner; they may even have the same name. However, <b>GetCustomAttributeByName</b> returns only one instance. (<b>GetCustomAttributeByName</b> returns the first instance that it encounters.) To find all instances of a custom attribute, call the <a href="https://msdn.microsoft.com/d5ecb71e-a52f-421b-aab9-48efcc77ec2f">EnumCustomAttributes</a> method.






## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

