---
UID: NF:objidlbase.IInternalUnknown.QueryInternalInterface
title: IInternalUnknown::QueryInternalInterface (objidlbase.h)
description: The IInternalUnknown::QueryInternalInterface (objidlbase.h) method retrieves pointers to the supported internal interfaces on an object.
helpviewer_keywords: ["IInternalUnknown interface [COM]","QueryInternalInterface method","IInternalUnknown.QueryInternalInterface","IInternalUnknown::QueryInternalInterface","QueryInternalInterface","QueryInternalInterface method [COM]","QueryInternalInterface method [COM]","IInternalUnknown interface","_com_iinternalunknown_queryinternalinterface","com.iinternalunknown_queryinternalinterface","objidlbase/IInternalUnknown::QueryInternalInterface"]
old-location: com\iinternalunknown_queryinternalinterface.htm
tech.root: com
ms.assetid: 7fa3478a-126c-43d9-851f-effa016c33f2
ms.date: 08/13/2022
ms.keywords: IInternalUnknown interface [COM],QueryInternalInterface method, IInternalUnknown.QueryInternalInterface, IInternalUnknown::QueryInternalInterface, QueryInternalInterface, QueryInternalInterface method [COM], QueryInternalInterface method [COM],IInternalUnknown interface, _com_iinternalunknown_queryinternalinterface, com.iinternalunknown_queryinternalinterface, objidlbase/IInternalUnknown::QueryInternalInterface
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
 - IInternalUnknown::QueryInternalInterface
 - objidlbase/IInternalUnknown::QueryInternalInterface
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
 - IInternalUnknown.QueryInternalInterface
---

# IInternalUnknown::QueryInternalInterface


## -description

Retrieves pointers to the supported internal interfaces on an object.

## -parameters

### -param riid [in]

The identifier of the internal interface being requested.

### -param ppv [out]

The address of a pointer variable that receives the interface pointer requested in the <i>riid</i> parameter. Upon successful return, *<i>ppv</i> contains the requested interface pointer to the object. If the object does not support the interface, *<i>ppv</i> is set to <b>NULL</b>.

## -returns

This method returns S_OK if the interface is supported, and E_NOINTERFACE otherwise.

## -remarks

This method is similar to the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method, except that the COM proxy manager, when aggregated, will not expose some interfaces through <b>QueryInterface</b>. Instead, those internal interfaces must be exposed through <b>QueryInternalInterface</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iinternalunknown">IInternalUnknown</a>



<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
