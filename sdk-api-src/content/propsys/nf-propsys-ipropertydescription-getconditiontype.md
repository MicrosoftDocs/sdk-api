---
UID: NF:propsys.IPropertyDescription.GetConditionType
title: IPropertyDescription::GetConditionType
author: windows-sdk-content
description: Gets the condition type and default condition operation to use when displaying the property in the query builder UI. This influences the list of predicate conditions (for example, equals, less than, and contains) that are shown for this property.
old-location: properties\IPropertyDescription_GetConditionType.htm
tech.root: properties
ms.assetid: d71bfed8-22e4-4dde-ba88-4bedfe07af62
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetConditionType, GetConditionType method [Windows Properties], GetConditionType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetConditionType method, IPropertyDescription.GetConditionType, IPropertyDescription::GetConditionType, properties.IPropertyDescription_GetConditionType, propsys/IPropertyDescription::GetConditionType, shell.IPropertyDescription_GetConditionType, shell_IPropertyDescription_GetConditionType
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
 - IPropertyDescription.GetConditionType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescription::GetConditionType


## -description


Gets the condition type and default condition operation to use when displaying the property in the query builder UI. This influences the list of predicate conditions (for example, equals, less than, and contains) that are shown for this property.


## -parameters




### -param pcontype [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762523(v=VS.85).aspx">PROPDESC_CONDITION_TYPE</a>*</b>

A pointer to a value that indicates the condition type.


### -param popDefault [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>*</b>

When this method returns, contains a pointer to a value that indicates the default condition operation.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



For more information, see the <i>conditionType</i> attribute of the <a href="https://msdn.microsoft.com/en-us/library/Bb773889(v=VS.85).aspx">typeInfo</a> element in the property's .propdesc file.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

