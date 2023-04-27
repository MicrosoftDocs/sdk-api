---
UID: NF:comcat.IEnumCATEGORYINFO.Clone
title: IEnumCATEGORYINFO::Clone (comcat.h)
description: Creates a new enumerator that contains the same enumeration state as the current one. (IEnumCATEGORYINFO.Clone)
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumCATEGORYINFO interface","IEnumCATEGORYINFO interface [COM]","Clone method","IEnumCATEGORYINFO.Clone","IEnumCATEGORYINFO::Clone","_com_ienumcategoryinfo_clone","com.ienumcategoryinfo_clone","comcat/IEnumCATEGORYINFO::Clone"]
old-location: com\ienumcategoryinfo_clone.htm
tech.root: com
ms.assetid: 9179b417-7dcd-4bb4-832f-86830e4b77ad
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumCATEGORYINFO interface, IEnumCATEGORYINFO interface [COM],Clone method, IEnumCATEGORYINFO.Clone, IEnumCATEGORYINFO::Clone, _com_ienumcategoryinfo_clone, com.ienumcategoryinfo_clone, comcat/IEnumCATEGORYINFO::Clone
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Comcat.idl
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
 - IEnumCATEGORYINFO::Clone
 - comcat/IEnumCATEGORYINFO::Clone
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
 - IEnumCATEGORYINFO.Clone
---

# IEnumCATEGORYINFO::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppenum [out]

A pointer to the cloned enumerator object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-ienumcategoryinfo">IEnumCATEGORYINFO</a>
