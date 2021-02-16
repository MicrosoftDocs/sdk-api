---
UID: NF:comsvcs.IContextProperties.SetProperty
title: IContextProperties::SetProperty (comsvcs.h)
description: Sets a context object property.
helpviewer_keywords: ["IContextProperties interface [COM+]","SetProperty method","IContextProperties.SetProperty","IContextProperties::SetProperty","SetProperty","SetProperty method [COM+]","SetProperty method [COM+]","IContextProperties interface","_cos_IContextProperties_SetProperty","comsvcs/IContextProperties::SetProperty","cos.icontextproperties_setproperty"]
old-location: cos\icontextproperties_setproperty.htm
tech.root: cos
ms.assetid: 4f6a27a2-37e9-4d4b-9d7e-916d791f03a5
ms.date: 12/05/2018
ms.keywords: IContextProperties interface [COM+],SetProperty method, IContextProperties.SetProperty, IContextProperties::SetProperty, SetProperty, SetProperty method [COM+], SetProperty method [COM+],IContextProperties interface, _cos_IContextProperties_SetProperty, comsvcs/IContextProperties::SetProperty, cos.icontextproperties_setproperty
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
 - IContextProperties::SetProperty
 - comsvcs/IContextProperties::SetProperty
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
 - IContextProperties.SetProperty
---

# IContextProperties::SetProperty


## -description

Sets a context object property.

## -parameters

### -param name [in]

The name of the context object property to be set. See <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icontextproperties-getproperty">GetProperty</a> for a list of valid property names.

### -param property [in]

The context object property value.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextproperties">IContextProperties</a>