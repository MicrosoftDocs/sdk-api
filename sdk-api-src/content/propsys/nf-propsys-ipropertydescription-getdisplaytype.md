---
UID: NF:propsys.IPropertyDescription.GetDisplayType
title: IPropertyDescription::GetDisplayType
author: windows-sdk-content
description: Gets the current data type used to display the property.
old-location: properties\IPropertyDescription_GetDisplayType.htm
tech.root: properties
ms.assetid: e3147b06-0849-4b49-8153-e120e2220651
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDisplayType, GetDisplayType method [Windows Properties], GetDisplayType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetDisplayType method, IPropertyDescription.GetDisplayType, IPropertyDescription::GetDisplayType, PDDT_BOOLEAN (0x00000002), PDDT_DATETIME (0x00000003), PDDT_ENUMERATED (0x00000004), PDDT_NUMBER (0x00000001), PDDT_STRING (0x00000000), properties.IPropertyDescription_GetDisplayType, propsys/IPropertyDescription::GetDisplayType, shell.IPropertyDescription_GetDisplayType, shell_IPropertyDescription_GetDisplayType
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.GetDisplayType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescription::GetDisplayType


## -description


Gets the current data type used to display the property.


## -parameters




### -param pdisplaytype [out]

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
                    Use <a href="https://msdn.microsoft.com/library/Bb761539(v=VS.85).aspx">IPropertyDescription::GetEnumTypeList</a> to handle this type.
                    


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



The value retrieved by this method is originally set through the <i>displayType</i> attribute of the <a href="https://msdn.microsoft.com/en-us/library/Bb773865(v=VS.85).aspx">displayInfo</a> element in the property's .propdesc file.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

