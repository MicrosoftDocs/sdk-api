---
UID: NN:msctf.ITfPersistentPropertyLoaderACP
title: ITfPersistentPropertyLoaderACP (msctf.h)
description: The ITfPersistentPropertyLoaderACP interface is implemented by an application and used by the TSF manager to load properties asynchronously.
helpviewer_keywords: ["ITfPersistentPropertyLoaderACP","ITfPersistentPropertyLoaderACP interface [Text Services Framework]","ITfPersistentPropertyLoaderACP interface [Text Services Framework]","described","_tsf_itfpersistentpropertyloaderacp_ref","msctf/ITfPersistentPropertyLoaderACP","tsf.itfpersistentpropertyloaderacp"]
old-location: tsf\itfpersistentpropertyloaderacp.htm
tech.root: TSF
ms.assetid: 7d7af737-6241-43a9-946e-6a03a423b20f
ms.date: 12/05/2018
ms.keywords: ITfPersistentPropertyLoaderACP, ITfPersistentPropertyLoaderACP interface [Text Services Framework], ITfPersistentPropertyLoaderACP interface [Text Services Framework],described, _tsf_itfpersistentpropertyloaderacp_ref, msctf/ITfPersistentPropertyLoaderACP, tsf.itfpersistentpropertyloaderacp
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfPersistentPropertyLoaderACP
 - msctf/ITfPersistentPropertyLoaderACP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfPersistentPropertyLoaderACP
---

# ITfPersistentPropertyLoaderACP interface


## -description

The <b>ITfPersistentPropertyLoaderACP</b> interface is implemented by an application and used by the TSF manager to load properties asynchronously. An application passes an instance of this interface when calling <a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize</a>. When properties are loaded by a call to <b>ITextStoreACPServices::Unserialize</b> , this interface is used to load properties when required rather than all at once.

## -inheritance

The <b>ITfPersistentPropertyLoaderACP</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfPersistentPropertyLoaderACP</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
