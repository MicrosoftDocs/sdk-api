---
UID: NF:strmif.IMediaFilter.GetState
title: IMediaFilter::GetState (strmif.h)
author: windows-sdk-content
description: The GetState method retrieves the filters's state (running, stopped, or paused).
old-location: dshow\imediafilter_getstate.htm
tech.root: DirectShow
ms.assetid: b20ca3e9-bec2-4c6d-ba80-f4dae2f5a831
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IBaseFilter interface, GetState method [DirectShow],IMediaFilter interface, IBaseFilter interface [DirectShow],GetState method, IBaseFilter::GetState, IMediaFilter interface [DirectShow],GetState method, IMediaFilter.GetState, IMediaFilter::GetState, IMediaFilterGetState, dshow.imediafilter_getstate, strmif/IBaseFilter::GetState, strmif/IMediaFilter::GetState
ms.topic: method
f1_keywords: 
 - "strmif/IMediaFilter.GetState"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMediaFilter.GetState
 - IBaseFilter.GetState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaFilter::GetState


## -description


The <b>GetState</b> method retrieves the filters's state (running, stopped, or paused). 
      


## -parameters




### -param dwMilliSecsTimeout [in]

Time-out interval, in milliseconds. To block indefinitely, use the value <b>INFINITE</b>.


### -param State [out]

Receives a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-filter_state">FILTER_STATE</a> enumerated type, indicating the filter's state.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_STATE_INTERMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
Intermediate state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_CANT_CUE</b></dt>
</dl>
</td>
<td width="60%">
The filter is active, but cannot deliver data.

</td>
</tr>
</table>
 




## -remarks



State transitions can be asynchronous. If the filter is transitioning to a new state, and the method times out before the transition completes, the method returns <b>VFW_S_STATE_INTERMEDIATE</b>.

If a filter cannot deliver data for some reason, it returns <b>VFW_S_CANT_CUE</b>. Live capture filters return this value while paused, because they do not deliver data in the paused state.

For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter Interface</a>
 

 

