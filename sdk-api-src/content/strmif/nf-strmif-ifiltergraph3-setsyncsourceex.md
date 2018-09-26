---
UID: NF:strmif.IFilterGraph3.SetSyncSourceEx
title: IFilterGraph3::SetSyncSourceEx
author: windows-sdk-content
description: The SetSyncSourceEx method establishes two reference clocks for the filter graph:\_a primary clock that is used by most of the filters, and a secondary clock that is used only by one specified filter.
old-location: dshow\ifiltergraph3_setsyncsourceex.htm
tech.root: DirectShow
ms.assetid: 153a0584-d613-499d-8dbb-c4207c7f60b3
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IFilterGraph3 interface [DirectShow],SetSyncSourceEx method, IFilterGraph3.SetSyncSourceEx, IFilterGraph3::SetSyncSourceEx, IFilterGraph3SetSyncSourceEx, SetSyncSourceEx, SetSyncSourceEx method [DirectShow], SetSyncSourceEx method [DirectShow],IFilterGraph3 interface, dshow.ifiltergraph3_setsyncsourceex, strmif/IFilterGraph3::SetSyncSourceEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFilterGraph3.SetSyncSourceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterGraph3::SetSyncSourceEx


## -description



The <code>SetSyncSourceEx</code> method establishes two reference clocks for the filter graph: a primary clock that is used by most of the filters, and a secondary clock that is used only by one specified filter.




## -parameters




### -param pClockForMostOfFilterGraph [in]

Pointer to the <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a> interface of the main reference clock. Every filter in the graph uses this clock, except for the filter specified by the <i>pFilter</i> parameter.


### -param pClockForFilter [in]

Pointer to the <b>IReferenceClock</b> interface of the secondary clock. The filter specified by the <i>pFilter</i> parameter uses this clock.


### -param pFilter [in]

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of a filter in the graph. This filter uses the secondary reference clock.


## -returns



Returns and <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not stopped.

</td>
</tr>
</table>
 




## -remarks



If the filter graph is running or paused, this method return VFW_E_NOT_STOPPED.

To clear both reference clocks, set all three parameters to <b>NULL</b>. To set a single clock for the entire graph, with no secondary clock, call the <a href="https://msdn.microsoft.com/a374c963-cc28-41f6-814d-7ffc6efc67a6">IMediaFilter::SetSyncSource</a> method on the Filter Graph Manager.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1d5f8eda-2b09-4627-8ae9-f43f38c3c26a">IFilterGraph3 Interface</a>
 

 

