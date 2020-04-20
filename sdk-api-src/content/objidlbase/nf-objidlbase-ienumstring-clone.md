---
UID: NF:objidlbase.IEnumString.Clone
title: IEnumString::Clone (objidlbase.h)
description: Creates a new enumerator that contains the same enumeration state as the current one.helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumString interface","IEnumString interface [COM]","Clone method","IEnumString.Clone","IEnumString::Clone","_com_ienumstring_clone","com.ienumstring_clone","objidlbase/IEnumString::Clone"]
old-location: com\ienumstring_clone.htm
tech.root: com
ms.assetid: d61ecfb3-9f3b-45ee-9872-9a92240f1234
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumString interface, IEnumString interface [COM],Clone method, IEnumString.Clone, IEnumString::Clone, _com_ienumstring_clone, com.ienumstring_clone, objidlbase/IEnumString::Clone
f1_keywords:
- objidlbase/IEnumString.Clone
dev_langs:
- c++
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IEnumString.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumString::Clone


## -description


Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.


## -parameters




### -param ppenum [out]

A pointer to the cloned enumerator object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>
 

 

