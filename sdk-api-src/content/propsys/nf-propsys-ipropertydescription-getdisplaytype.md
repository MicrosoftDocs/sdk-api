---
UID: NF:propsys.IPropertyDescription.GetDisplayType
title: IPropertyDescription::GetDisplayType method
author: windows-driver-content
description: Gets the current data type used to display the property.
old-location: properties\IPropertyDescription_GetDisplayType.htm
old-project: properties
ms.assetid: e3147b06-0849-4b49-8153-e120e2220651
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetDisplayType method [Windows Properties], GetDisplayType method [Windows Properties], IPropertyDescription interface, GetDisplayType,IPropertyDescription.GetDisplayType, IPropertyDescription, IPropertyDescription interface [Windows Properties], GetDisplayType method, IPropertyDescription::GetDisplayType, PDDT_BOOLEAN (0x00000002), PDDT_DATETIME (0x00000003), PDDT_ENUMERATED (0x00000004), PDDT_NUMBER (0x00000001), PDDT_STRING (0x00000000), properties.IPropertyDescription_GetDisplayType, propsys/IPropertyDescription::GetDisplayType, shell.IPropertyDescription_GetDisplayType, shell_IPropertyDescription_GetDisplayType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyDescription.GetDisplayType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyDescription::GetDisplayType method


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
 

 

