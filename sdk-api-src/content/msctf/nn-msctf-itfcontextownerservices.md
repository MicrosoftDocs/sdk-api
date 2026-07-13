---
UID: NN:msctf.ITfContextOwnerServices
title: ITfContextOwnerServices (msctf.h)
description: The ITfContextOwnerServices interface is implemented by the manager and used by a text service or application acting as context owners.
helpviewer_keywords: ["ITfContextOwnerServices","ITfContextOwnerServices interface [Text Services Framework]","ITfContextOwnerServices interface [Text Services Framework]","described","_tsf_itfcontextownerservices_ref","msctf/ITfContextOwnerServices","tsf.itfcontextownerservices"]
old-location: tsf\itfcontextownerservices.htm
tech.root: TSF
ms.assetid: fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerServices, ITfContextOwnerServices interface [Text Services Framework], ITfContextOwnerServices interface [Text Services Framework],described, _tsf_itfcontextownerservices_ref, msctf/ITfContextOwnerServices, tsf.itfcontextownerservices
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
 - ITfContextOwnerServices
 - msctf/ITfContextOwnerServices
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
 - ITfContextOwnerServices
---

# ITfContextOwnerServices interface


## -description

The <b>ITfContextOwnerServices</b> interface is implemented by the manager and used by a text service or application acting as context owners. The interface provides notification changes to sinks and other services to context owners that do not implement the <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> or <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a> interfaces. Clients obtain this interface by calling the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext::QueryInterface</a> method.

## -inheritance

The <b>ITfContextOwnerServices</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextOwnerServices</b> also has these types of members:

