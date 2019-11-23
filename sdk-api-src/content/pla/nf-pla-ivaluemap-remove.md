---
UID: NF:pla.IValueMap.Remove
title: IValueMap::Remove (pla.h)

description: Removes an item from the collection.
old-location: pla\ivaluemap_remove.htm
tech.root: PLA
ms.assetid: dc674243-ec0f-496f-bffb-faf4262a42c7

ms.date: 12/05/2018
ms.keywords: IValueMap interface [PLA],Remove method, IValueMap.Remove, IValueMap::Remove, Remove, Remove method [PLA], Remove method [PLA],IValueMap interface, base.ivaluemap_remove, pla.ivaluemap_remove, pla/IValueMap::Remove
ms.topic: method
f1_keywords: 
 - "pla/IValueMap.Remove"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IValueMap.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IValueMap::Remove


## -description


Removes an item from the collection.


## -parameters




### -param value [in]

The zero-based index of the item to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface to be removed.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-add">IValueMap::Add</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-clear">IValueMap::Clear</a>
 

 

