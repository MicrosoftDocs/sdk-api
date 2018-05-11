---
UID: NF:segment.IMSVidStreamBufferSink3.get_CCCounter
title: IMSVidStreamBufferSink3::get_CCCounter
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersink3_get_cccounter.htm
old-project: mstv
ms.assetid: 76c3e3e5-521a-40d3-98b9-c5a757fc2bec
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],get_CCCounter method, IMSVidStreamBufferSink3.get_CCCounter, IMSVidStreamBufferSink3::get_CCCounter, IMSVidStreamBufferSink3get_CCCounter, get_CCCounter, get_CCCounter method [Microsoft TV Technologies], get_CCCounter method [Microsoft TV Technologies],IMSVidStreamBufferSink3 interface, mstv.imsvidstreambuffersink3_get_cccounter, segment/IMSVidStreamBufferSink3::get_CCCounter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferSink3.get_CCCounter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferSink3::get_CCCounter


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_CCCounter</b> method enables the caller to get performance statistics from the Stream Buffer Sink for the closed captioning stream.


## -parameters




### -param ppUnk [out]

Receives a pointer to the <b>IUnknown</b> interface. Query this pointer for the <a href="https://msdn.microsoft.com/d9394d04-ba6b-4946-b33a-9c53070238f7">IStreamBufferDataCounters</a> interface. The caller must release the <b>IUnknown</b> interface.


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




<a href="https://msdn.microsoft.com/5768936b-9c0a-4177-82da-cc6ebe62ea67">IMSVidStreamBufferSink3 Interface</a>
 

 

