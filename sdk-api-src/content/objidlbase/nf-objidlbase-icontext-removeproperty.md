---
UID: NF:objidlbase.IContext.RemoveProperty
title: IContext::RemoveProperty (objidlbase.h)
description: The IContext::RemoveProperty (objidlbase.h) method removes the specified context property from the context.
helpviewer_keywords: ["IContext interface [COM]","RemoveProperty method","IContext.RemoveProperty","IContext::RemoveProperty","RemoveProperty","RemoveProperty method [COM]","RemoveProperty method [COM]","IContext interface","_com_icontext_removeproperty","com.icontext_removeproperty","objidlbase/IContext::RemoveProperty"]
old-location: com\icontext_removeproperty.htm
tech.root: com
ms.assetid: bb5b282a-d337-4371-b1c2-1b429a5bf135
ms.date: 08/13/2022
ms.keywords: IContext interface [COM],RemoveProperty method, IContext.RemoveProperty, IContext::RemoveProperty, RemoveProperty, RemoveProperty method [COM], RemoveProperty method [COM],IContext interface, _com_icontext_removeproperty, com.icontext_removeproperty, objidlbase/IContext::RemoveProperty
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
 - IContext::RemoveProperty
 - objidlbase/IContext::RemoveProperty
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
 - IContext.RemoveProperty
---

# IContext::RemoveProperty


## -description

Removes the specified context property from the context.

## -parameters

### -param rPolicyId [in]

The GUID that uniquely identifies the context property to be removed.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-icontext">IContext</a>
