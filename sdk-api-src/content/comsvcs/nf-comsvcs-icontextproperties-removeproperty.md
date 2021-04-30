---
UID: NF:comsvcs.IContextProperties.RemoveProperty
title: IContextProperties::RemoveProperty (comsvcs.h)
description: Removes a context object property.
helpviewer_keywords: ["IContextProperties interface [COM+]","RemoveProperty method","IContextProperties.RemoveProperty","IContextProperties::RemoveProperty","RemoveProperty","RemoveProperty method [COM+]","RemoveProperty method [COM+]","IContextProperties interface","_cos_IContextProperties_RemoveProperty","comsvcs/IContextProperties::RemoveProperty","cos.icontextproperties_removeproperty"]
old-location: cos\icontextproperties_removeproperty.htm
tech.root: cos
ms.assetid: 112c9e08-de15-4e46-934a-5e57a1a52adc
ms.date: 12/05/2018
ms.keywords: IContextProperties interface [COM+],RemoveProperty method, IContextProperties.RemoveProperty, IContextProperties::RemoveProperty, RemoveProperty, RemoveProperty method [COM+], RemoveProperty method [COM+],IContextProperties interface, _cos_IContextProperties_RemoveProperty, comsvcs/IContextProperties::RemoveProperty, cos.icontextproperties_removeproperty
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
 - IContextProperties::RemoveProperty
 - comsvcs/IContextProperties::RemoveProperty
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
 - IContextProperties.RemoveProperty
---

# IContextProperties::RemoveProperty


## -description

Removes a context object property.

## -parameters

### -param name [in]

The name of the context object property to be removed. See <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icontextproperties-getproperty">GetProperty</a> for a list of valid property names.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextproperties">IContextProperties</a>