---
UID: NF:comsvcs.IGetContextProperties.GetProperty
title: IGetContextProperties::GetProperty (comsvcs.h)
description: Retrieves the value of the specified context property.
helpviewer_keywords: ["GetProperty","GetProperty method [COM+]","GetProperty method [COM+]","IGetContextProperties interface","IGetContextProperties interface [COM+]","GetProperty method","IGetContextProperties.GetProperty","IGetContextProperties::GetProperty","_cos_IGetContextProperties_GetProperty","comsvcs/IGetContextProperties::GetProperty","cos.igetcontextproperties_getproperty"]
old-location: cos\igetcontextproperties_getproperty.htm
tech.root: cos
ms.assetid: 920938a9-44b1-4473-8204-1129b9599a72
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [COM+], GetProperty method [COM+],IGetContextProperties interface, IGetContextProperties interface [COM+],GetProperty method, IGetContextProperties.GetProperty, IGetContextProperties::GetProperty, _cos_IGetContextProperties_GetProperty, comsvcs/IGetContextProperties::GetProperty, cos.igetcontextproperties_getproperty
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
 - IGetContextProperties::GetProperty
 - comsvcs/IGetContextProperties::GetProperty
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
 - IGetContextProperties.GetProperty
---

# IGetContextProperties::GetProperty


## -description

Retrieves the value of the specified context property.

## -parameters

### -param name [in]

The name of a current context property.

### -param pProperty [out, retval]

The value(s) of the property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetcontextproperties">IGetContextProperties</a>