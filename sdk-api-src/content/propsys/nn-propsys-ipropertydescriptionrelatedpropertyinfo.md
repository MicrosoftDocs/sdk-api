---
UID: NN:propsys.IPropertyDescriptionRelatedPropertyInfo
title: IPropertyDescriptionRelatedPropertyInfo (propsys.h)
description: Provides a method that retrieves an IPropertyDescription interface.
helpviewer_keywords: ["IPropertyDescriptionRelatedPropertyInfo","IPropertyDescriptionRelatedPropertyInfo interface [Windows Properties]","IPropertyDescriptionRelatedPropertyInfo interface [Windows Properties]","described","properties.IPropertyDescriptionRelatedPropertyInfo","propsys/IPropertyDescriptionRelatedPropertyInfo","shell.IPropertyDescriptionRelatedPropertyInfo","shell_IPropertyDescriptionRelatedPropertyInfo"]
old-location: properties\IPropertyDescriptionRelatedPropertyInfo.htm
tech.root: properties
ms.assetid: 1658542e-ca2f-4566-b40f-8647577f4481
ms.date: 12/05/2018
ms.keywords: IPropertyDescriptionRelatedPropertyInfo, IPropertyDescriptionRelatedPropertyInfo interface [Windows Properties], IPropertyDescriptionRelatedPropertyInfo interface [Windows Properties],described, properties.IPropertyDescriptionRelatedPropertyInfo, propsys/IPropertyDescriptionRelatedPropertyInfo, shell.IPropertyDescriptionRelatedPropertyInfo, shell_IPropertyDescriptionRelatedPropertyInfo
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescriptionRelatedPropertyInfo
 - propsys/IPropertyDescriptionRelatedPropertyInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionRelatedPropertyInfo
---

# IPropertyDescriptionRelatedPropertyInfo interface


## -description

Provides a method that retrieves an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface.

## -inheritance

The <b>IPropertyDescriptionRelatedPropertyInfo</b> interface inherits from <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>. <b>IPropertyDescriptionRelatedPropertyInfo</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface. There is only one implementation of <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo">IPropertyDescriptionRelatedPropertyInfo</a> in the system; it is provided by the Shell. 

Only one property description exists for each property in the system.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>
