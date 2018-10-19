---
UID: NF:msctf.ITfMouseTracker.AdviseMouseSink
title: ITfMouseTracker::AdviseMouseSink
author: windows-sdk-content
description: ITfMouseTracker::AdviseMouseSink method
old-location: tsf\itfmousetracker_advisemousesink.htm
tech.root: TSF
ms.assetid: d73b2b9b-8904-4507-9b32-dcb8946fb887
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: AdviseMouseSink, AdviseMouseSink method [Text Services Framework], AdviseMouseSink method [Text Services Framework],ITfMouseTracker interface, ITfMouseTracker interface [Text Services Framework],AdviseMouseSink method, ITfMouseTracker.AdviseMouseSink, ITfMouseTracker::AdviseMouseSink, _tsf_itfmousetracker_advisemousesink_ref, msctf/ITfMouseTracker::AdviseMouseSink, tsf.itfmousetracker_advisemousesink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfMouseTracker.AdviseMouseSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfMouseTracker::AdviseMouseSink


## -description




## -parameters




### -param range [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that specifies the range of text that the mouse sink is installed for.


### -param pSink [in]

Pointer to the <a href="https://msdn.microsoft.com/d6e5549e-768d-47af-a553-84430641cda4">ITfMouseSink</a> interface.


### -param pdwCookie [out]

Pointer to a DWORD value that receives a cookie that identifies the mouse event sink.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The context owner does not support mouse event sinks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



When the advise sink is installed, a mouse event that occurs over the range specified by <i>range</i> will result in the mouse event sink <a href="https://msdn.microsoft.com/1aa4fdb7-b16d-4e58-934a-8323450f6749">ITfMouseSink::OnMouseEvent</a> call.

The value placed in <i>pdwCookie</i> must be saved and passed to <a href="https://msdn.microsoft.com/7707b7ce-662b-43e5-ada4-ba42eec56ede">ITfMouseTracker::UnadviseMouseSink</a> to remove the mouse event sink.




## -see-also




<a href="https://msdn.microsoft.com/d6e5549e-768d-47af-a553-84430641cda4">ITfMouseSink
      </a>



<a href="https://msdn.microsoft.com/1aa4fdb7-b16d-4e58-934a-8323450f6749">ITfMouseSink::OnMouseEvent
      </a>



<a href="https://msdn.microsoft.com/aad07b35-99e0-4c76-ba65-93c2c972303d">ITfMouseTracker</a>



<a href="https://msdn.microsoft.com/7707b7ce-662b-43e5-ada4-ba42eec56ede">ITfMouseTracker::UnadviseMouseSink
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

