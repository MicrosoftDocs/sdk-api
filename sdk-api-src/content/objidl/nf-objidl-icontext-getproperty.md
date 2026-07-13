---
UID: NF:objidl.IContext.GetProperty
title: IContext::GetProperty (objidl.h)
description: The IContext::GetProperty method (objidl.h) retrieves the specified context property from the context.
helpviewer_keywords: ["GetProperty","GetProperty method [COM]","GetProperty method [COM]","IContext interface","IContext interface [COM]","GetProperty method","IContext.GetProperty","IContext::GetProperty","_com_icontext_getproperty","com.icontext_getproperty","objidlbase/IContext::GetProperty"]
old-location: com\icontext_getproperty.htm
tech.root: com
ms.assetid: 76c6f790-9103-4cee-8a67-0f69b00ba0a1
ms.date: 08/12/2022
ms.keywords: GetProperty, GetProperty method [COM], GetProperty method [COM],IContext interface, IContext interface [COM],GetProperty method, IContext.GetProperty, IContext::GetProperty, _com_icontext_getproperty, com.icontext_getproperty, objidlbase/IContext::GetProperty
req.header: objidl.h
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
 - IContext::GetProperty
 - objidl/IContext::GetProperty
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
 - IContext.GetProperty
---

# IContext::GetProperty


## -description

Retrieves the specified context property from the context.

## -parameters

### -param rGuid [in]

The GUID that uniquely identifies the context property to be retrieved.

### -param pFlags [out]

The address of the variable that receives the flags associated with the property.

### -param ppUnk [out]

The address of the variable that receives the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer of the requested context property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-icontext">IContext</a>
