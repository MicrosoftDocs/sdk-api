---
UID: NF:propsys.PSCreateSimplePropertyChange
title: PSCreateSimplePropertyChange function (propsys.h)
description: Creates a simple property change.
helpviewer_keywords: ["PSCreateSimplePropertyChange","PSCreateSimplePropertyChange function [Windows Properties]","_shell_PSCreateSimplePropertyChange","properties.PSCreateSimplePropertyChange","propsys/PSCreateSimplePropertyChange","shell.PSCreateSimplePropertyChange"]
old-location: properties\PSCreateSimplePropertyChange.htm
tech.root: properties
ms.assetid: d0bec600-47bd-481c-94b2-ffdff4f2c09b
ms.date: 12/05/2018
ms.keywords: PSCreateSimplePropertyChange, PSCreateSimplePropertyChange function [Windows Properties], _shell_PSCreateSimplePropertyChange, properties.PSCreateSimplePropertyChange, propsys/PSCreateSimplePropertyChange, shell.PSCreateSimplePropertyChange
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSCreateSimplePropertyChange
 - propsys/PSCreateSimplePropertyChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSCreateSimplePropertyChange
---

# PSCreateSimplePropertyChange function


## -description

Creates a simple property change.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-pka_flags">PKA_FLAGS</a></b>


<a href="/windows/desktop/api/propsys/ne-propsys-pka_flags">PKA_FLAGS</a> flags.

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param riid [in]

Type: <b>REFIID</b>

Reference to a specified IID.

### -param ppv [out]

Type: <b>void**</b>

The address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychange">IPropertyChange</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Property changes can be placed into an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychangearray">IPropertyChangeArray</a> which can then be used with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> to modify the properties on an item.