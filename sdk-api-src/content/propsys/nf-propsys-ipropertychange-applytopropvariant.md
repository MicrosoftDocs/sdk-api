---
UID: NF:propsys.IPropertyChange.ApplyToPropVariant
title: IPropertyChange::ApplyToPropVariant (propsys.h)
description: Applies a change to a property value.
helpviewer_keywords: ["ApplyToPropVariant","ApplyToPropVariant method [Windows Properties]","ApplyToPropVariant method [Windows Properties]","IPropertyChange interface","IPropertyChange interface [Windows Properties]","ApplyToPropVariant method","IPropertyChange.ApplyToPropVariant","IPropertyChange::ApplyToPropVariant","_shell_IPropertyChange_ApplyToPropVariant","properties.IPropertyChange_ApplyToPropVariant","propsys/IPropertyChange::ApplyToPropVariant","shell.IPropertyChange_ApplyToPropVariant"]
old-location: properties\IPropertyChange_ApplyToPropVariant.htm
tech.root: properties
ms.assetid: 7d7b6de5-0ed9-44fc-b2b3-c0f4cd8bf9c5
ms.date: 12/05/2018
ms.keywords: ApplyToPropVariant, ApplyToPropVariant method [Windows Properties], ApplyToPropVariant method [Windows Properties],IPropertyChange interface, IPropertyChange interface [Windows Properties],ApplyToPropVariant method, IPropertyChange.ApplyToPropVariant, IPropertyChange::ApplyToPropVariant, _shell_IPropertyChange_ApplyToPropVariant, properties.IPropertyChange_ApplyToPropVariant, propsys/IPropertyChange::ApplyToPropVariant, shell.IPropertyChange_ApplyToPropVariant
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
 - IPropertyChange::ApplyToPropVariant
 - propsys/IPropertyChange::ApplyToPropVariant
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
 - IPropertyChange.ApplyToPropVariant
---

# IPropertyChange::ApplyToPropVariant


## -description

Applies a change to a property value.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

A reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param ppropvarOut [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a changed <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertychange">IPropertyChange</a>



<a href="/windows/desktop/api/propsys/nf-propsys-pscreatesimplepropertychange">PSCreateSimplePropertyChange</a>