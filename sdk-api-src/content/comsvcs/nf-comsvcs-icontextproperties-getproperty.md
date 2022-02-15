---
UID: NF:comsvcs.IContextProperties.GetProperty
title: IContextProperties::GetProperty (comsvcs.h)
description: Retrieves a context object property.
helpviewer_keywords: ["GetProperty","GetProperty method [COM+]","GetProperty method [COM+]","IContextProperties interface","IContextProperties interface [COM+]","GetProperty method","IContextProperties.GetProperty","IContextProperties::GetProperty","_cos_IContextProperties_GetProperty","comsvcs/IContextProperties::GetProperty","cos.icontextproperties_getproperty"]
old-location: cos\icontextproperties_getproperty.htm
tech.root: cos
ms.assetid: dc7748b4-5cf4-41c6-af7d-82b2478b084c
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [COM+], GetProperty method [COM+],IContextProperties interface, IContextProperties interface [COM+],GetProperty method, IContextProperties.GetProperty, IContextProperties::GetProperty, _cos_IContextProperties_GetProperty, comsvcs/IContextProperties::GetProperty, cos.icontextproperties_getproperty
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
 - IContextProperties::GetProperty
 - comsvcs/IContextProperties::GetProperty
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
 - IContextProperties.GetProperty
---

# IContextProperties::GetProperty


## -description

Retrieves a context object property.

## -parameters

### -param name [in]

The name of the context object property to be retrieved.

The following are IIS intrinsic properties.

<ul>
<li>Application</li>
<li>Request</li>
<li>Response</li>
<li>Server</li>
<li>Session</li>
</ul>
The following is the COMTI intrinsic property:

<ul>
<li>host-security-callback.cedar.microsoft.com</li>
</ul>

### -param pProperty [out]

A pointer to the property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

To retrieve an IIS object, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> using the VT_DISPATCH member of the returned <b>VARIANT</b> for the interface to the IIS object (for example, IResponse for the Response object).

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextproperties">IContextProperties</a>