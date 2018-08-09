---
UID: NF:strmif.IFilterChain.RemoveChain
title: IFilterChain::RemoveChain
author: windows-sdk-content
description: The RemoveChain method removes every filter in a filter chain from the filter graph.
old-location: dshow\ifilterchain_removechain.htm
old-project: DirectShow
ms.assetid: a47d2087-5f06-4fce-b573-16935370a34c
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IFilterChain interface [DirectShow],RemoveChain method, IFilterChain.RemoveChain, IFilterChain::RemoveChain, IFilterChainRemoveChain, RemoveChain, RemoveChain method [DirectShow], RemoveChain method [DirectShow],IFilterChain interface, dshow.ifilterchain_removechain, strmif/IFilterChain::RemoveChain
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterChain::RemoveChain


## -description



The <code>RemoveChain</code> method removes every filter in a filter chain from the filter graph.




## -parameters




### -param pStartFilter [in]

A pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter at the start of the chain.


### -param pEndFilter [in]

A pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the failure otherwise.




## -remarks



You can call this method while the graph is running; the method stops the filters in the chain before removing them from the graph.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/04fa1e89-19cd-488e-9df2-8a5fd2c3f445">IFilterChain Interface</a>
 

 

