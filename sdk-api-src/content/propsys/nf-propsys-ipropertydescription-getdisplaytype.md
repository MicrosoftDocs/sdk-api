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

# IPropertyDescription::GetDisplayType


## -description


Gets the current data type used to display the property.


## -parameters




### -param pdisplaytype






#### - pdt [out]

Type: <b>PROPDESC_DISPLAYTYPE*</b>

Contains a pointer to a value that indicates the display type. One of the following values.



#### PDDT_STRING (0x00000000) (0)

The value is displayed as a string.



#### PDDT_NUMBER (0x00000001) (1)

The value is displayed as an integer.



#### PDDT_BOOLEAN (0x00000002) (2)

The value is displayed as a Boolean value.



#### PDDT_DATETIME (0x00000003) (3)

The value is displayed as date and time.



#### PDDT_ENUMERATED (0x00000004) (4)

The value is displayed as an enumerated type-list.
                    Use <a href="shell.IPropertyDescription_GetEnumTypeList">IPropertyDescription::GetEnumTypeList</a> to handle this type.
                    


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



The value retrieved by this method is originally set through the <i>displayType</i> attribute of the <a href="shell.propdesc_schema_displayInfo">displayInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

