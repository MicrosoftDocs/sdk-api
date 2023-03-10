---
UID: NF:objidlbase.IEnumContextProps.Clone
title: IEnumContextProps::Clone (objidlbase.h)
description: The IEnumContextProps::Clone (objidlbase.h) method creates a new enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumContextProps interface","IEnumContextProps interface [COM]","Clone method","IEnumContextProps.Clone","IEnumContextProps::Clone","_com_ienumcontextprops_clone","com.ienumcontextprops_clone","objidlbase/IEnumContextProps::Clone"]
old-location: com\ienumcontextprops_clone.htm
tech.root: com
ms.assetid: 0bf7f7da-9e40-49bd-9bd0-d2fcdfc2f517
ms.date: 08/13/2022
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumContextProps interface, IEnumContextProps interface [COM],Clone method, IEnumContextProps.Clone, IEnumContextProps::Clone, _com_ienumcontextprops_clone, com.ienumcontextprops_clone, objidlbase/IEnumContextProps::Clone
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
 - IEnumContextProps::Clone
 - objidlbase/IEnumContextProps::Clone
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
 - IEnumContextProps.Clone
---

# IEnumContextProps::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppEnumContextProps [out]

A pointer to the cloned enumerator object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumcontextprops">IEnumContextProps</a>
