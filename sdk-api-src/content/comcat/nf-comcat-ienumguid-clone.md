---
UID: NF:comcat.IEnumGUID.Clone
title: IEnumGUID::Clone (comcat.h)
description: Creates a new enumerator that contains the same enumeration state as the current one. (IEnumGUID.Clone)
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumGUID interface","IEnumGUID interface [COM]","Clone method","IEnumGUID.Clone","IEnumGUID::Clone","_com_ienumguid_clone","com.ienumguid_clone","comcat/IEnumGUID::Clone"]
old-location: com\ienumguid_clone.htm
tech.root: com
ms.assetid: 5b12adf2-c2fe-4499-ab2a-94af6337e4a2
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumGUID interface, IEnumGUID interface [COM],Clone method, IEnumGUID.Clone, IEnumGUID::Clone, _com_ienumguid_clone, com.ienumguid_clone, comcat/IEnumGUID::Clone
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
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
 - IEnumGUID::Clone
 - comcat/IEnumGUID::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - IEnumGUID.Clone
---

# IEnumGUID::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppenum [out]

A pointer to the cloned enumerator object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-ienumguid">IEnumGUID</a>
