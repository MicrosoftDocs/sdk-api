---
UID: NF:unknwn.IUnknown.QueryInterface(Q)
title: IUnknown::QueryInterface(Q,)
description: A helper function template that infers an interface identifier, and calls [QueryInterface(REFIID,void)](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)).
helpviewer_keywords: ["IUnknown interface [COM]","QueryInterface method","IUnknown.QueryInterface","IUnknown.QueryInterface(Q",")","IUnknown::QueryInterface","IUnknown::QueryInterface(Q",")","QueryInterface","QueryInterface method [COM]","QueryInterface method [COM]","IUnknown interface","_com_iunknown_queryinterface","com.iunknown_queryinterface","unknwn/IUnknown::QueryInterface"]
old-location: com\iunknown_queryinterface.htm
tech.root: com
ms.assetid: 54d5ff80-18db-43f2-b636-f93ac053146d
ms.date: 05/31/2019
ms.keywords: IUnknown interface [COM],QueryInterface method, IUnknown.QueryInterface, IUnknown.QueryInterface(Q,), IUnknown::QueryInterface, IUnknown::QueryInterface(Q,), QueryInterface, QueryInterface method [COM], QueryInterface method [COM],IUnknown interface, _com_iunknown_queryinterface, com.iunknown_queryinterface, unknwn/IUnknown::QueryInterface
req.header: unknwn.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
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
 - IUnknown::QueryInterface
 - unknwn/IUnknown::QueryInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Unknwn.h
api_name:
 - IUnknown.QueryInterface
---

## -description

A helper function template that infers an interface identifier, and calls [QueryInterface(REFIID,void)](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)).

## -parameters

### -param pp [out]

Type: **[void](/windows/desktop/winprog/windows-data-types)\*\***

The address of a pointer to an interface. For details, see the *ppvObject* parameter of [QueryInterface(REFIID,void)](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)).

## -returns

The function passes the return value back from [QueryInterface(REFIID,void)](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)).

## -syntax

```cpp
template<class Q>
HRESULT
STDMETHODCALLTYPE
QueryInterface(_COM_Outptr_ Q** pp)
{
    return QueryInterface(__uuidof(Q), (void **)pp);
}
```

The `class Q` template parameter is the type of a COM interface.

## -see-also

* [IUnknown interface](/windows/desktop/api/unknwn/nn-unknwn-iunknown)

