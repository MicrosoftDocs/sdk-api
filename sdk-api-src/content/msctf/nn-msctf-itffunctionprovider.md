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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFunctionProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFunctionProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFunctionProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Obtains the description of the function provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">GetFunction</a>
</td>
<td align="left" width="63%">
Obtains the specified function object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-gettype">GetType</a>
</td>
<td align="left" width="63%">
Obtains the type identifier for the function provider.

</td>
</tr>
</table>

## -remarks

A function provider is registered by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITFSourceSingle::AdviseSingleSink</a> with IID_ITfFunctionProvider when the text service is activated. The text service should unregister its function provider with <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-unadvisesinglesink">ITFSourceSingle::UnadviseSingleSink</a> when it is deactivated.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITFSourceSingle::AdviseSingleSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-unadvisesinglesink">ITFSourceSingle::UnadviseSingleSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

