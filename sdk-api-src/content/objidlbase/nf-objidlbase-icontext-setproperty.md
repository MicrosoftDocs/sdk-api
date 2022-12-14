---
UID: NF:objidlbase.IContext.SetProperty
title: IContext::SetProperty (objidlbase.h)
description: The IContext::SetProperty (objidlbase.h) method adds the specified context property to the object context.
helpviewer_keywords: ["IContext interface [COM]","SetProperty method","IContext.SetProperty","IContext::SetProperty","SetProperty","SetProperty method [COM]","SetProperty method [COM]","IContext interface","_com_icontext_setproperty","com.icontext_setproperty","objidlbase/IContext::SetProperty"]
old-location: com\icontext_setproperty.htm
tech.root: com
ms.assetid: 8e6dc055-bc97-41e0-973c-b061e851daf5
ms.date: 08/13/2022
ms.keywords: IContext interface [COM],SetProperty method, IContext.SetProperty, IContext::SetProperty, SetProperty, SetProperty method [COM], SetProperty method [COM],IContext interface, _com_icontext_setproperty, com.icontext_setproperty, objidlbase/IContext::SetProperty
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IContext::SetProperty
 - objidlbase/IContext::SetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IContext.SetProperty
---

# IContext::SetProperty


## -description

Adds the specified context property to the object context.

## -parameters

### -param rpolicyId [in]

A GUID that uniquely identifies this context property.

### -param flags [in]

This parameter is reserved and must be zero.

### -param pUnk [in]

A pointer to the context property to be added.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-icontext">IContext</a>
