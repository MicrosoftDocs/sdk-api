---
UID: NF:pla.IValueMap.Add
title: IValueMap::Add (pla.h)
description: Adds an item to the collection. (IValueMap.Add)
helpviewer_keywords: ["Add","Add method [PLA]","Add method [PLA]","IValueMap interface","IValueMap interface [PLA]","Add method","IValueMap.Add","IValueMap::Add","base.ivaluemap_add","pla.ivaluemap_add","pla/IValueMap::Add"]
old-location: pla\ivaluemap_add.htm
tech.root: PLA
ms.assetid: 4a6f074d-8d18-44ea-bbbc-8d3a7f6c033a
ms.date: 12/05/2018
ms.keywords: Add, Add method [PLA], Add method [PLA],IValueMap interface, IValueMap interface [PLA],Add method, IValueMap.Add, IValueMap::Add, base.ivaluemap_add, pla.ivaluemap_add, pla/IValueMap::Add
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IValueMap::Add
 - pla/IValueMap::Add
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IValueMap.Add
---

# IValueMap::Add


## -description

Adds an item to the collection.

## -parameters

### -param value [in]

An <b>IDispatch</b> interface of the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface to add to the collection. The variant type is VT_DISPATCH. 

You can also add a string or integer value. If the value is an integer (the variant type is VT_I4, VT_UI4, VT_I8, or VT_UI8), PLA adds an item with the specified value. 

If the value is a string  (the variant type is VT_BSTR), PLA tries to convert the string to an integer. If successful, PLA adds an item with the specified integer value. If PLA cannot convert the string, PLA searches the collection for a key that matches the string. If found, PLA enables the item; otherwise, the add fails.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-addrange">IValueMap::AddRange</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-remove">IValueMap::Remove</a>
