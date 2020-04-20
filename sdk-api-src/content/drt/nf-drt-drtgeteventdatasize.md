---
UID: NF:drt.DrtGetEventDataSize
title: DrtGetEventDataSize function (drt.h)
description: DrtGetEventDataSize function returns the size of the DRT_EVENT_DATA structure associated with a signaled event.helpviewer_keywords: ["DrtGetEventDataSize","DrtGetEventDataSize function [Peer Networking]","drt/DrtGetEventDataSize","p2p.drtgeteventdatasize"]
old-location: p2p\drtgeteventdatasize.htm
tech.root: P2PSdk
ms.assetid: b73431fc-6b5a-41f7-8616-6d82dc8844f4
ms.date: 12/05/2018
ms.keywords: DrtGetEventDataSize, DrtGetEventDataSize function [Peer Networking], drt/DrtGetEventDataSize, p2p.drtgeteventdatasize
f1_keywords:
- drt/DrtGetEventDataSize
dev_langs:
- c++
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- drt.dll
api_name:
- DrtGetEventDataSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrtGetEventDataSize function


## -description


The <b>DrtGetEventDataSize</b> function returns the size of the <a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_event_data">DRT_EVENT_DATA</a> structure associated with a signaled event.


## -parameters




### -param hDrt [in]

Handle to the Distributed Routing Table instance for which the event occurred.


### -param pulEventDataLen [out]

The size, in bytes, of the event data.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT infrastructure is unaware of the requested search.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pulEventDataLen</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hDrt</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_NO_MORE</b></dt>
</dl>
</td>
<td width="60%">
There is no more event data available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_event_data">DRT_EVENT_DATA</a>
 

 

