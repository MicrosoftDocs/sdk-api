---
UID: NN:msctf.ITextStoreACPServices
title: ITextStoreACPServices (msctf.h)
description: The ITextStoreACPServices interface is implemented by the TSF manager to provide various services to an ACP-based application.
helpviewer_keywords: ["ITextStoreACPServices","ITextStoreACPServices interface [Text Services Framework]","ITextStoreACPServices interface [Text Services Framework]","described","_tsf_itextstoreacpservices_ref","msctf/ITextStoreACPServices","tsf.itextstoreacpservices"]
old-location: tsf\itextstoreacpservices.htm
tech.root: TSF
ms.assetid: 8c84429c-3f99-4ab1-b994-e4e93cd9c86d
ms.date: 12/05/2018
ms.keywords: ITextStoreACPServices, ITextStoreACPServices interface [Text Services Framework], ITextStoreACPServices interface [Text Services Framework],described, _tsf_itextstoreacpservices_ref, msctf/ITextStoreACPServices, tsf.itextstoreacpservices
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
 - ITextStoreACPServices
 - msctf/ITextStoreACPServices
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
 - ITextStoreACPServices
---

# ITextStoreACPServices interface


## -description

The <b>ITextStoreACPServices</b> interface is implemented by the TSF manager to provide various services to an ACP-based application. To obtain an instance of this interface, an application calls <b>QueryInterface</b> on the <i>punk</i> parameter passed to <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink</a> with IID_ITextStoreACPServices.

## -inheritance

The <b>ITextStoreACPServices</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACPServices</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
