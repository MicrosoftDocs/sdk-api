---
UID: NF:strmif.IFilterChain.PauseChain
title: IFilterChain::PauseChain
author: windows-sdk-content
description: The PauseChain method switches all the filters in a filter chain into a paused state.
old-location: dshow\ifilterchain_pausechain.htm
tech.root: DirectShow
ms.assetid: a153ebf6-1d0a-45d0-ad2a-eb1eda62da2c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IFilterChain interface [DirectShow],PauseChain method, IFilterChain.PauseChain, IFilterChain::PauseChain, IFilterChainPauseChain, PauseChain, PauseChain method [DirectShow], PauseChain method [DirectShow],IFilterChain interface, dshow.ifilterchain_pausechain, strmif/IFilterChain::PauseChain
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
 - IFilterChain.PauseChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterChain::PauseChain


## -description



The <code>PauseChain</code> method switches all the filters in a filter chain into a paused state.




## -parameters




### -param pStartFilter [in]

A pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter at the start of the chain.


### -param pEndFilter [in]

A pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.


## -returns



Returns S_OK if successful. If the method fails, the return value may be VFW_E_NOT_PAUSED or another <b>HRESULT</b> value.




## -remarks



If this method cannot switch a given filter into a paused state, it stops all of the filters in chain. The filter graph must be paused when you call this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/04fa1e89-19cd-488e-9df2-8a5fd2c3f445">IFilterChain Interface</a>
 

 

