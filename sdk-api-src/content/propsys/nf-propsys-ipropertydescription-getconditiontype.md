---
UID: NF:propsys.IPropertyDescription.GetConditionType
title: IPropertyDescription::GetConditionType
author: windows-sdk-content
description: Gets the condition type and default condition operation to use when displaying the property in the query builder UI. This influences the list of predicate conditions (for example, equals, less than, and contains) that are shown for this property.
old-location: properties\IPropertyDescription_GetConditionType.htm
old-project: properties
ms.assetid: d71bfed8-22e4-4dde-ba88-4bedfe07af62
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetConditionType, GetConditionType method [Windows Properties], GetConditionType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetConditionType method, IPropertyDescription.GetConditionType, IPropertyDescription::GetConditionType, properties.IPropertyDescription_GetConditionType, propsys/IPropertyDescription::GetConditionType, shell.IPropertyDescription_GetConditionType, shell_IPropertyDescription_GetConditionType
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PSC_STATE
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription::GetConditionType


## -description


Gets the condition type and default condition operation to use when displaying the property in the query builder UI. This influences the list of predicate conditions (for example, equals, less than, and contains) that are shown for this property.


## -parameters




### -param pcontype [out]

Type: <b><a href="shell.PROPDESC_CONDITION_TYPE">PROPDESC_CONDITION_TYPE</a>*</b>

A pointer to a value that indicates the condition type.


### -param popDefault [out]

Type: <b><a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>*</b>

When this method returns, contains a pointer to a value that indicates the default condition operation.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



For more information, see the <i>conditionType</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

