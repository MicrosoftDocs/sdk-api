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

# IPropertyDescription::GetRelativeDescriptionType


## -description


Gets the relative description type for a property description.


## -parameters




### -param prdt [out]

Type: <b><a href="shell.PROPDESC_RELATIVEDESCRIPTION_TYPE">PROPDESC_RELATIVEDESCRIPTION_TYPE</a>*</b>

When this method returns, contains a pointer to the relative description type value. See <a href="shell.PROPDESC_RELATIVEDESCRIPTION_TYPE">PROPDESC_RELATIVEDESCRIPTION_TYPE</a> for valid values.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



The information retrieved by this method comes from the <i>relativeDescriptionType</i> attribute of the <a href="shell.propdesc_schema_displayInfo">displayInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

