---
UID: NF:objidl.IContext.EnumContextProps
title: IContext::EnumContextProps (objidl.h)
description: The IContext::EnumContextProps method (objidl.h) returns an IEnumContextProps interface pointer that can enumerate the context properties in this context.
helpviewer_keywords: ["EnumContextProps","EnumContextProps method [COM]","EnumContextProps method [COM]","IContext interface","IContext interface [COM]","EnumContextProps method","IContext.EnumContextProps","IContext::EnumContextProps","_com_icontext_enumcontextprops","com.icontext_enumcontextprops","objidlbase/IContext::EnumContextProps"]
old-location: com\icontext_enumcontextprops.htm
tech.root: com
ms.assetid: 7cae291e-dcf3-43b1-8306-9e5c7a5d3be0
ms.date: 08/12/2022
ms.keywords: EnumContextProps, EnumContextProps method [COM], EnumContextProps method [COM],IContext interface, IContext interface [COM],EnumContextProps method, IContext.EnumContextProps, IContext::EnumContextProps, _com_icontext_enumcontextprops, com.icontext_enumcontextprops, objidlbase/IContext::EnumContextProps
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
 - IContext::EnumContextProps
 - objidl/IContext::EnumContextProps
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
 - IContext.EnumContextProps
---

# IContext::EnumContextProps


## -description

Returns an <a href="/windows/desktop/api/objidl/nn-objidl-ienumcontextprops">IEnumContextProps</a> interface pointer that can be used to enumerate the context properties in this context.

## -parameters

### -param ppEnumContextProps [out]

The address of the variable that receives the new <a href="/windows/desktop/api/objidl/nn-objidl-ienumcontextprops">IEnumContextProps</a> interface pointer.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-icontext">IContext</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumcontextprops">IEnumContextProps</a>
