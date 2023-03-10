---
UID: NF:comsvcs.IContextProperties.EnumNames
title: IContextProperties::EnumNames (comsvcs.h)
description: Retrieves a reference to an enumerator for the context object properties.
helpviewer_keywords: ["EnumNames","EnumNames method [COM+]","EnumNames method [COM+]","IContextProperties interface","IContextProperties interface [COM+]","EnumNames method","IContextProperties.EnumNames","IContextProperties::EnumNames","_cos_IContextProperties_EnumNames","comsvcs/IContextProperties::EnumNames","cos.icontextproperties_enumnames"]
old-location: cos\icontextproperties_enumnames.htm
tech.root: cos
ms.assetid: cae9eaf7-a422-4daa-9f0a-e7863f167112
ms.date: 12/05/2018
ms.keywords: EnumNames, EnumNames method [COM+], EnumNames method [COM+],IContextProperties interface, IContextProperties interface [COM+],EnumNames method, IContextProperties.EnumNames, IContextProperties::EnumNames, _cos_IContextProperties_EnumNames, comsvcs/IContextProperties::EnumNames, cos.icontextproperties_enumnames
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IContextProperties::EnumNames
 - comsvcs/IContextProperties::EnumNames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IContextProperties.EnumNames
---

# IContextProperties::EnumNames


## -description

Retrieves a reference to an enumerator for the context object properties.

## -parameters

### -param ppenum [out]

A reference to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a> interface on a new enumerator object that you can use to iterate through all the context object properties.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Use the <b>EnumNames</b> method to obtain a reference to an enumerator object. The returned <a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a> interface exposes several methods you can use to iterate through a list of <b>BSTR</b> values representing context object properties. When you have a name, you can use the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icontextproperties-getproperty">GetProperty</a> method to obtain a reference to the context object property it represents. As with any COM object, you must release an enumerator object when you are finished using it.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextproperties">IContextProperties</a>