---
UID: NN:msctf.ITfCreatePropertyStore
title: ITfCreatePropertyStore (msctf.h)
description: The ITfCreatePropertyStore interface is implemented by a text service to support persistence of property store data.
helpviewer_keywords: ["ITfCreatePropertyStore","ITfCreatePropertyStore interface [Text Services Framework]","ITfCreatePropertyStore interface [Text Services Framework]","described","_tsf_itfcreatepropertystore_ref","msctf/ITfCreatePropertyStore","tsf.itfcreatepropertystore"]
old-location: tsf\itfcreatepropertystore.htm
tech.root: TSF
ms.assetid: f21619c5-5f59-4cc4-9f84-fa5f8a178d40
ms.date: 12/05/2018
ms.keywords: ITfCreatePropertyStore, ITfCreatePropertyStore interface [Text Services Framework], ITfCreatePropertyStore interface [Text Services Framework],described, _tsf_itfcreatepropertystore_ref, msctf/ITfCreatePropertyStore, tsf.itfcreatepropertystore
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCreatePropertyStore
 - msctf/ITfCreatePropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfCreatePropertyStore
---

# ITfCreatePropertyStore interface


## -description

The <b>ITfCreatePropertyStore</b> interface is implemented by a text service to support persistence of property store data. The TSF manager uses this interface to determine if a property store can be serialized and to create a property store object for a serialized property.

## -inheritance

The <b>ITfCreatePropertyStore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCreatePropertyStore</b> also has these types of members:

## -remarks

When a property store is unserialized, the TSF manager creates an object from the CLSID obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfpropertystore-gettype">ITfPropertyStore::GetPropertyRangeCreator</a> and obtain an <b>ITfCreatePropertyStore</b> interface pointer from it. The manager then uses <b>ITfCreatePropertyStore::CreatePropertyStore</b> to create the property store object.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfpropertystore-getpropertyrangecreator">ITfPropertyStore::GetPropertyRangeCreator
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
