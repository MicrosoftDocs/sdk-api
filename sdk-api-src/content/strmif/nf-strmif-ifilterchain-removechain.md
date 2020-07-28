---
UID: NF:strmif.IFilterChain.RemoveChain
title: IFilterChain::RemoveChain (strmif.h)
description: The RemoveChain method removes every filter in a filter chain from the filter graph.
helpviewer_keywords: ["IFilterChain interface [DirectShow]","RemoveChain method","IFilterChain.RemoveChain","IFilterChain::RemoveChain","IFilterChainRemoveChain","RemoveChain","RemoveChain method [DirectShow]","RemoveChain method [DirectShow]","IFilterChain interface","dshow.ifilterchain_removechain","strmif/IFilterChain::RemoveChain"]
old-location: dshow\ifilterchain_removechain.htm
tech.root: dshow
ms.assetid: a47d2087-5f06-4fce-b573-16935370a34c
ms.date: 12/05/2018
ms.keywords: IFilterChain interface [DirectShow],RemoveChain method, IFilterChain.RemoveChain, IFilterChain::RemoveChain, IFilterChainRemoveChain, RemoveChain, RemoveChain method [DirectShow], RemoveChain method [DirectShow],IFilterChain interface, dshow.ifilterchain_removechain, strmif/IFilterChain::RemoveChain
f1_keywords:
- strmif/IFilterChain.RemoveChain
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IFilterChain.RemoveChain
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterChain::RemoveChain


## -description



The <code>RemoveChain</code> method removes every filter in a filter chain from the filter graph.




## -parameters




### -param pStartFilter [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the start of the chain.


### -param pEndFilter [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the failure otherwise.




## -remarks



You can call this method while the graph is running; the method stops the filters in the chain before removing them from the graph.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilterchain">IFilterChain Interface</a>
 

 

