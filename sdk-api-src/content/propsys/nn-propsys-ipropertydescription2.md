---
UID: NN:propsys.IPropertyDescription2
title: IPropertyDescription2 (propsys.h)
description: Exposes methods that enumerate and retrieve individual property description details. (IPropertyDescription2)
helpviewer_keywords: ["IPropertyDescription2","IPropertyDescription2 interface [Windows Properties]","IPropertyDescription2 interface [Windows Properties]","described","properties.IPropertyDescription2","propsys/IPropertyDescription2","shell.IPropertyDescription2","shell_IPropertyDescription2"]
old-location: properties\IPropertyDescription2.htm
tech.root: properties
ms.assetid: 46c009b0-caf7-469f-9973-36d100a5ef98
ms.date: 12/05/2018
ms.keywords: IPropertyDescription2, IPropertyDescription2 interface [Windows Properties], IPropertyDescription2 interface [Windows Properties],described, properties.IPropertyDescription2, propsys/IPropertyDescription2, shell.IPropertyDescription2, shell_IPropertyDescription2
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
 - IPropertyDescription2
 - propsys/IPropertyDescription2
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
 - IPropertyDescription2
---

# IPropertyDescription2 interface


## -description

Exposes methods that enumerate and retrieve individual property description details.

## -inheritance

The <b>IPropertyDescription2</b> interface inherits from <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>. <b>IPropertyDescription2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface, from which it inherits.

To obtain this interface, call <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescription">PSGetPropertyDescription</a>, <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionbyname">PSGetPropertyDescriptionByName</a>, or <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionlist-getat">IPropertyDescriptionList::GetAt</a>.

Only one property description exists for each property in the system.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface. There is only one implementation of <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> in the system; it is provided by the Shell.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>
