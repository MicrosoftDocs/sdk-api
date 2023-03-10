---
UID: NN:propsys.IPropertyDescription
title: IPropertyDescription (propsys.h)
description: Exposes methods that enumerate and retrieve individual property description details. (IPropertyDescription)
helpviewer_keywords: ["IPropertyDescription","IPropertyDescription interface [Windows Properties]","IPropertyDescription interface [Windows Properties]","described","properties.IPropertyDescription","propsys/IPropertyDescription","shell.IPropertyDescription","shell_IPropertyDescription"]
old-location: properties\IPropertyDescription.htm
tech.root: properties
ms.assetid: 9abd476c-450e-4381-b28e-afca00d4b179
ms.date: 12/05/2018
ms.keywords: IPropertyDescription, IPropertyDescription interface [Windows Properties], IPropertyDescription interface [Windows Properties],described, properties.IPropertyDescription, propsys/IPropertyDescription, shell.IPropertyDescription, shell_IPropertyDescription
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescription
 - propsys/IPropertyDescription
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
 - IPropertyDescription
---

# IPropertyDescription interface


## -description

Exposes methods that enumerate and retrieve individual property description details.

## -inheritance

The <b>IPropertyDescription</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyDescription</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface. There is only one implementation of <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> in the system; it is provided by the Shell. 

To obtain this interface, call <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescription">PSGetPropertyDescription</a>, <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionbyname">PSGetPropertyDescriptionByName</a>, or <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionlist-getat">IPropertyDescriptionList::GetAt</a>.

Only one property description exists for each property in the system.

## -see-also

<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>
