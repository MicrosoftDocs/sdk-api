---
UID: NF:strmif.IGraphConfig.PushThroughData
title: IGraphConfig::PushThroughData
author: windows-sdk-content
description: The PushThroughData method pushes data through the filter graph to the specified pin.
old-location: dshow\igraphconfig_pushthroughdata.htm
old-project: DirectShow
ms.assetid: f3d72a32-f43a-4a61-b25e-6d472aa629de
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IGraphConfig interface [DirectShow],PushThroughData method, IGraphConfig.PushThroughData, IGraphConfig::PushThroughData, IGraphConfigPushThroughData, PushThroughData, PushThroughData method [DirectShow], PushThroughData method [DirectShow],IGraphConfig interface, dshow.igraphconfig_pushthroughdata, strmif/IGraphConfig::PushThroughData
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
 - IGraphConfig.PushThroughData
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphConfig::PushThroughData


## -description



The <code>PushThroughData</code> method pushes data through the filter graph to the specified pin.




## -parameters




### -param pOutputPin [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of an output pin in the filter graph.


### -param pConnection [in]

Pointer to the <a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection</a> interface of an input pin in the filter graph. This parameter can be <b>NULL</b>.


### -param hEventAbort [in]

Handle to an event. If the caller is a filter calling on one of its data processing threads, this parameter should be a handle to an event that will be signaled when the filter is put into a stopped state. Otherwise, this parameter can be <b>NULL</b>. For more information, see Remarks.


## -returns



Returns S_OK if successful. Otherwise, returns an error code that may be one of the following values, or others not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find a candidate input pin.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_STATE_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
Filter state changed during the operation.

</td>
</tr>
</table>
 




## -remarks



This method pushes through any pending data, from a specified output pin down to a specified input pin. Optionally, you can leave the input pin unspecified and let the method search the filter graph for the best candidate. Do not call this method from the thread that is pushing data.

If a filter calls this method on one of its own data processing threads, it creates the potential for a deadlock. The method obtains a lock on the filter graph, which can block the filter from stopping on receiving a call to <a href="https://msdn.microsoft.com/8c415b5c-1aee-4ea4-b182-fd95da4898aa">IMediaFilter::Stop</a>. To prevent this situation, the method takes a handle to an event object provided by the filter. The filter should signal the event if it receives a call to its <b>Stop</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>
 

 

