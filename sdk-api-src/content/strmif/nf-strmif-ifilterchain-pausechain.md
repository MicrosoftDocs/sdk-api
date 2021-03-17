---
UID: NF:strmif.IFilterChain.PauseChain
title: IFilterChain::PauseChain (strmif.h)
description: The PauseChain method switches all the filters in a filter chain into a paused state.
helpviewer_keywords: ["IFilterChain interface [DirectShow]","PauseChain method","IFilterChain.PauseChain","IFilterChain::PauseChain","IFilterChainPauseChain","PauseChain","PauseChain method [DirectShow]","PauseChain method [DirectShow]","IFilterChain interface","dshow.ifilterchain_pausechain","strmif/IFilterChain::PauseChain"]
old-location: dshow\ifilterchain_pausechain.htm
tech.root: dshow
ms.assetid: a153ebf6-1d0a-45d0-ad2a-eb1eda62da2c
ms.date: 12/05/2018
ms.keywords: IFilterChain interface [DirectShow],PauseChain method, IFilterChain.PauseChain, IFilterChain::PauseChain, IFilterChainPauseChain, PauseChain, PauseChain method [DirectShow], PauseChain method [DirectShow],IFilterChain interface, dshow.ifilterchain_pausechain, strmif/IFilterChain::PauseChain
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
 - IFilterChain::PauseChain
 - strmif/IFilterChain::PauseChain
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
 - IFilterChain.PauseChain
---

# IFilterChain::PauseChain


## -description

The <code>PauseChain</code> method switches all the filters in a filter chain into a paused state.

## -parameters

### -param pStartFilter [in]

A pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the start of the chain.

### -param pEndFilter [in]

A pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.

## -returns

Returns S_OK if successful. If the method fails, the return value may be VFW_E_NOT_PAUSED or another <b>HRESULT</b> value.

## -remarks

If this method cannot switch a given filter into a paused state, it stops all of the filters in chain. The filter graph must be paused when you call this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilterchain">IFilterChain Interface</a>