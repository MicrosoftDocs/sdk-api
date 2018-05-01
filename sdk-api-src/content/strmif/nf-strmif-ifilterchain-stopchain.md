---
UID: NF:strmif.IFilterChain.StopChain
title: IFilterChain::StopChain method
author: windows-driver-content
description: The StopChain method switches all the filters in a filter chain into a stopped state.
old-location: dshow\ifilterchain_stopchain.htm
old-project: DirectShow
ms.assetid: 03821fdb-8374-4386-868b-9bf7b2d83562
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IFilterChain, IFilterChain interface [DirectShow], StopChain method, IFilterChain::StopChain, IFilterChainStopChain, StopChain method [DirectShow], StopChain method [DirectShow], IFilterChain interface, StopChain,IFilterChain.StopChain, dshow.ifilterchain_stopchain, strmif/IFilterChain::StopChain
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFilterChain.StopChain
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterChain::StopChain method


## -description



The <code>StopChain</code> method switches all the filters in a filter chain into a stopped state.




## -parameters




### -param pStartFilter [in]

A pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter at the start of the chain.


### -param pEndFilter [in]

Pointer to the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the failure otherwise.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/04fa1e89-19cd-488e-9df2-8a5fd2c3f445">IFilterChain Interface</a>
 

 

