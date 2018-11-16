---
UID: NF:strmif.IMediaFilter.GetState
title: IMediaFilter::GetState
author: windows-sdk-content
description: The GetState method retrieves the filters's state (running, stopped, or paused).
old-location: dshow\imediafilter_getstate.htm
tech.root: DirectShow
ms.assetid: b20ca3e9-bec2-4c6d-ba80-f4dae2f5a831
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IBaseFilter interface, GetState method [DirectShow],IMediaFilter interface, IBaseFilter interface [DirectShow],GetState method, IBaseFilter::GetState, IMediaFilter interface [DirectShow],GetState method, IMediaFilter.GetState, IMediaFilter::GetState, IMediaFilterGetState, dshow.imediafilter_getstate, strmif/IBaseFilter::GetState, strmif/IMediaFilter::GetState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IMediaFilter.GetState
: 
---

# IMediaFilter::GetState


## -description


The <b>GetState</b> method retrieves the filters's state (running, stopped, or paused). 
      


## -parameters




### -param dwMilliSecsTimeout [in]

Time-out interval, in milliseconds. To block indefinitely, use the value <b>INFINITE</b>.


### -param State [out]

Receives a member of the <a href="https://msdn.microsoft.com/41f88abc-57d1-4f80-a099-d17e624ab8a6">FILTER_STATE</a> enumerated type, indicating the filter's state.


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

For more information, see <a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a>



<a href="https://msdn.microsoft.com/5c0060e8-a9e5-4141-a38d-9a1bc55cc91b">IMediaFilter Interface</a>
 

 

