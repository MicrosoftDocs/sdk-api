---
UID: NF:segment.IMSVidStreamBufferSink3.get_CCCounter
title: IMSVidStreamBufferSink3::get_CCCounter (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.helpviewer_keywords: ["IMSVidStreamBufferSink3 interface [Microsoft TV Technologies]","get_CCCounter method","IMSVidStreamBufferSink3.get_CCCounter","IMSVidStreamBufferSink3::get_CCCounter","IMSVidStreamBufferSink3get_CCCounter","get_CCCounter","get_CCCounter method [Microsoft TV Technologies]","get_CCCounter method [Microsoft TV Technologies]","IMSVidStreamBufferSink3 interface","mstv.imsvidstreambuffersink3_get_cccounter","segment/IMSVidStreamBufferSink3::get_CCCounter"]
old-location: mstv\imsvidstreambuffersink3_get_cccounter.htm
tech.root: mstv
ms.assetid: 76c3e3e5-521a-40d3-98b9-c5a757fc2bec
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],get_CCCounter method, IMSVidStreamBufferSink3.get_CCCounter, IMSVidStreamBufferSink3::get_CCCounter, IMSVidStreamBufferSink3get_CCCounter, get_CCCounter, get_CCCounter method [Microsoft TV Technologies], get_CCCounter method [Microsoft TV Technologies],IMSVidStreamBufferSink3 interface, mstv.imsvidstreambuffersink3_get_cccounter, segment/IMSVidStreamBufferSink3::get_CCCounter
f1_keywords:
- segment/IMSVidStreamBufferSink3.get_CCCounter
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidStreamBufferSink3.get_CCCounter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSink3::get_CCCounter


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_CCCounter</b> method enables the caller to get performance statistics from the Stream Buffer Sink for the closed captioning stream.


## -parameters




### -param ppUnk [out]

Receives a pointer to the <b>IUnknown</b> interface. Query this pointer for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferdatacounters">IStreamBufferDataCounters</a> interface. The caller must release the <b>IUnknown</b> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersink3">IMSVidStreamBufferSink3 Interface</a>
 

 

