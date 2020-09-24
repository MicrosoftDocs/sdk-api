---
UID: NF:strmif.IFilterChain.StartChain
title: IFilterChain::StartChain (strmif.h)
description: The StartChain method switches all the filters in a filter chain into a running state.
helpviewer_keywords: ["IFilterChain interface [DirectShow]","StartChain method","IFilterChain.StartChain","IFilterChain::StartChain","IFilterChainStartChain","StartChain","StartChain method [DirectShow]","StartChain method [DirectShow]","IFilterChain interface","dshow.ifilterchain_startchain","strmif/IFilterChain::StartChain"]
old-location: dshow\ifilterchain_startchain.htm
tech.root: dshow
ms.assetid: 095a8c28-d0f2-4c0d-9e96-eefd5786b88d
ms.date: 12/05/2018
ms.keywords: IFilterChain interface [DirectShow],StartChain method, IFilterChain.StartChain, IFilterChain::StartChain, IFilterChainStartChain, StartChain, StartChain method [DirectShow], StartChain method [DirectShow],IFilterChain interface, dshow.ifilterchain_startchain, strmif/IFilterChain::StartChain
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
 - IFilterChain::StartChain
 - strmif/IFilterChain::StartChain
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
 - IFilterChain.StartChain
---

# IFilterChain::StartChain


## -description

The <code>StartChain</code> method switches all the filters in a filter chain into a running state.

## -parameters

### -param pStartFilter [in]

A pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the start of the chain.

### -param pEndFilter [in]

Pointer to the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.

## -returns

Returns S_OK if successful. If the method fails, the return value may be VFW_E_NOT_RUNNING or another <b>HRESULT</b> value.

## -remarks

If this method cannot switch a given filter into a running state, it leaves all the filters in a stopped state. The filter graph must be running when you call this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilterchain">IFilterChain Interface</a>