---
UID: NF:comsvcs.IObjectConstruct.Construct
title: IObjectConstruct::Construct (comsvcs.h)
description: Constructs an object using the specified parameters.
helpviewer_keywords: ["Construct","Construct method [COM+]","Construct method [COM+]","IObjectConstruct interface","IObjectConstruct interface [COM+]","Construct method","IObjectConstruct.Construct","IObjectConstruct::Construct","_cos_IObjectConstruct_Construct","comsvcs/IObjectConstruct::Construct","cos.iobjectconstruct_construct"]
old-location: cos\iobjectconstruct_construct.htm
tech.root: cos
ms.assetid: 6bbb25c7-bd60-46cb-baed-114c50feb1f3
ms.date: 12/05/2018
ms.keywords: Construct, Construct method [COM+], Construct method [COM+],IObjectConstruct interface, IObjectConstruct interface [COM+],Construct method, IObjectConstruct.Construct, IObjectConstruct::Construct, _cos_IObjectConstruct_Construct, comsvcs/IObjectConstruct::Construct, cos.iobjectconstruct_construct
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
 - IObjectConstruct::Construct
 - comsvcs/IObjectConstruct::Construct
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
 - IObjectConstruct.Construct
---

# IObjectConstruct::Construct


## -description

Constructs an object using the specified parameters.

## -parameters

### -param pCtorObj [in]

A reference to an implementation of the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstructstring">IObjectConstructString</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/cossdk/com--object-constructor-strings">COM+ Object Constructor Strings</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstruct">IObjectConstruct</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstructstring">IObjectConstructString</a>



<a href="/windows/desktop/cossdk/specifying-an-object-constructor-string-for-a-component">Specifying an Object Constructor String for a Component</a>