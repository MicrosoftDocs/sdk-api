---
UID: NF:strmif.IGraphConfig.RemoveFilterEx
title: IGraphConfig::RemoveFilterEx
author: windows-sdk-content
description: The RemoveFilterEx method removes a filter from the filter graph.
old-location: dshow\igraphconfig_removefilterex.htm
tech.root: DirectShow
ms.assetid: c3298aa2-4eb2-4e47-9f36-5f2cf541d13e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IGraphConfig interface [DirectShow],RemoveFilterEx method, IGraphConfig.RemoveFilterEx, IGraphConfig::RemoveFilterEx, IGraphConfigRemoveFilterEx, RemoveFilterEx, RemoveFilterEx method [DirectShow], RemoveFilterEx method [DirectShow],IGraphConfig interface, dshow.igraphconfig_removefilterex, strmif/IGraphConfig::RemoveFilterEx
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
 - IGraphConfig.RemoveFilterEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphConfig::RemoveFilterEx


## -description



The <code>RemoveFilterEx</code> method removes a filter from the filter graph.




## -parameters




### -param pFilter [in]

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter to remove from the graph.


### -param Flags [in]

Combination of flags from the <a href="https://msdn.microsoft.com/0bc91914-fa43-4ab7-a85e-30590a717c47">REM_FILTER_FLAGS</a> enumerated type.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the failure.




## -remarks



This method extends the <a href="https://msdn.microsoft.com/ec681340-0fb9-4eba-8211-d5fa07fb076b">IFilterGraph::RemoveFilter</a> method by accepting a flag that specifies the behavior of the method. This flag enables an application to remove a filter without disconnecting the pins automatically, which improves performance when moving groups of connected filters into a new graph.

By default, this method disconnects the filter before removing it from the graph. Use the REMFILTERF_LEAVECONNECTED flag to leave the filter connected.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>
 

 

