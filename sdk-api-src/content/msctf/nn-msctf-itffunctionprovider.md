---
UID: NN:msctf.ITfFunctionProvider
title: ITfFunctionProvider (msctf.h)
description: The ITfFunctionProvider interface is implemented by an application or text service to provide various function objects.
helpviewer_keywords: ["ITfFunctionProvider","ITfFunctionProvider interface [Text Services Framework]","ITfFunctionProvider interface [Text Services Framework]","described","_tsf_itffunctionprovider_ref","msctf/ITfFunctionProvider","tsf.itffunctionprovider"]
old-location: tsf\itffunctionprovider.htm
tech.root: TSF
ms.assetid: e63fd561-1157-49b1-a981-e578d9538876
ms.date: 12/05/2018
ms.keywords: ITfFunctionProvider, ITfFunctionProvider interface [Text Services Framework], ITfFunctionProvider interface [Text Services Framework],described, _tsf_itffunctionprovider_ref, msctf/ITfFunctionProvider, tsf.itffunctionprovider
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
 - ITfFunctionProvider
 - msctf/ITfFunctionProvider
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
 - ITfFunctionProvider
---

# ITfFunctionProvider interface


## -description

The <b>ITfFunctionProvider</b> interface is implemented by an application or text service to provide various function objects.

## -inheritance

The <b>ITfFunctionProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFunctionProvider</b> also has these types of members:

## -remarks

A function provider is registered by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITFSourceSingle::AdviseSingleSink</a> with IID_ITfFunctionProvider when the text service is activated. The text service should unregister its function provider with <a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-unadvisesinglesink">ITFSourceSingle::UnadviseSingleSink</a> when it is deactivated.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITFSourceSingle::AdviseSingleSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-unadvisesinglesink">ITFSourceSingle::UnadviseSingleSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
