---
UID: NF:msctf.ITfMouseTracker.UnadviseMouseSink
title: ITfMouseTracker::UnadviseMouseSink method
author: windows-driver-content
description: ITfMouseTracker::UnadviseMouseSink method
old-location: tsf\itfmousetracker_unadvisemousesink.htm
old-project: TSF
ms.assetid: 7707b7ce-662b-43e5-ada4-ba42eec56ede
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfMouseTracker, ITfMouseTracker interface [Text Services Framework], UnadviseMouseSink method, ITfMouseTracker::UnadviseMouseSink, UnadviseMouseSink method [Text Services Framework], UnadviseMouseSink method [Text Services Framework], ITfMouseTracker interface, UnadviseMouseSink,ITfMouseTracker.UnadviseMouseSink, _tsf_itfmousetracker_unadvisemousesink_ref, msctf/ITfMouseTracker::UnadviseMouseSink, tsf.itfmousetracker_unadvisemousesink
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfMouseTracker.UnadviseMouseSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfMouseTracker::UnadviseMouseSink method


## -description




## -parameters




### -param dwCookie [in]

Specifies the mouse advise sink identifier. This value is obtained by a call to <a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">ITfMouseTracker::AdviseMouseSink</a>.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/aad07b35-99e0-4c76-ba65-93c2c972303d">ITfMouseTracker</a>



<a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">ITfMouseTracker::AdviseMouseSink
      </a>
 

 

