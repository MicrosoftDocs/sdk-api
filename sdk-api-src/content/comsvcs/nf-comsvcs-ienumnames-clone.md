---
UID: NF:comsvcs.IEnumNames.Clone
title: IEnumNames::Clone (comsvcs.h)
description: Creates an enumerator that contains the same enumeration state as the current one. (IEnumNames.Clone)
helpviewer_keywords: ["Clone","Clone method [COM+]","Clone method [COM+]","IEnumNames interface","IEnumNames interface [COM+]","Clone method","IEnumNames.Clone","IEnumNames::Clone","_cos_IEnumNames_Clone","comsvcs/IEnumNames::Clone","cos.ienumnames_clone"]
old-location: cos\ienumnames_clone.htm
tech.root: cos
ms.assetid: ea57be73-076a-445d-9b0d-4a1041befa2d
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM+], Clone method [COM+],IEnumNames interface, IEnumNames interface [COM+],Clone method, IEnumNames.Clone, IEnumNames::Clone, _cos_IEnumNames_Clone, comsvcs/IEnumNames::Clone, cos.ienumnames_clone
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
 - IEnumNames::Clone
 - comsvcs/IEnumNames::Clone
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
 - IEnumNames.Clone
---

# IEnumNames::Clone


## -description

Creates an enumerator that contains the same enumeration state as the current one.

## -parameters

### -param ppenum [out]

Address of a pointer to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a> interface on the enumeration object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a>
