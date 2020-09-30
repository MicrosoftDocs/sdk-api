---
UID: NF:strmif.IFilterChain.StopChain
title: IFilterChain::StopChain (strmif.h)
description: The StopChain method switches all the filters in a filter chain into a stopped state.
helpviewer_keywords: ["IFilterChain interface [DirectShow]","StopChain method","IFilterChain.StopChain","IFilterChain::StopChain","IFilterChainStopChain","StopChain","StopChain method [DirectShow]","StopChain method [DirectShow]","IFilterChain interface","dshow.ifilterchain_stopchain","strmif/IFilterChain::StopChain"]
old-location: dshow\ifilterchain_stopchain.htm
tech.root: dshow
ms.assetid: 03821fdb-8374-4386-868b-9bf7b2d83562
ms.date: 12/05/2018
ms.keywords: IFilterChain interface [DirectShow],StopChain method, IFilterChain.StopChain, IFilterChain::StopChain, IFilterChainStopChain, StopChain, StopChain method [DirectShow], StopChain method [DirectShow],IFilterChain interface, dshow.ifilterchain_stopchain, strmif/IFilterChain::StopChain
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterChain::StopChain
 - strmif/IFilterChain::StopChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterChain.StopChain
---

# IFilterChain::StopChain


## -description

The <code>StopChain</code> method switches all the filters in a filter chain into a stopped state.

## -parameters

### -param pStartFilter [in]

A pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the start of the chain.

### -param pEndFilter [in]

Pointer to the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the failure otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilterchain">IFilterChain Interface</a>