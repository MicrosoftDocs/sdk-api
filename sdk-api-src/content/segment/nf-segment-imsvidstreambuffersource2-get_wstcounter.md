---
UID: NF:segment.IMSVidStreamBufferSource2.get_WSTCounter
title: IMSVidStreamBufferSource2::get_WSTCounter
author: windows-driver-content
description: The get_WSTCounter method enables the caller to get performance statistics from the Stream Buffer Source for the World Standard Teletext (WST) stream.
old-location: mstv\imsvidstreambuffersource2_get_wstcounter.htm
old-project: mstv
ms.assetid: a506a152-c0e7-497b-a494-5464f712f432
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidStreamBufferSource2 interface [Microsoft TV Technologies],get_WSTCounter method, IMSVidStreamBufferSource2.get_WSTCounter, IMSVidStreamBufferSource2::get_WSTCounter, IMSVidStreamBufferSource2get_WSTCounter, get_WSTCounter, get_WSTCounter method [Microsoft TV Technologies], get_WSTCounter method [Microsoft TV Technologies],IMSVidStreamBufferSource2 interface, mstv.imsvidstreambuffersource2_get_wstcounter, segment/IMSVidStreamBufferSource2::get_WSTCounter
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
-	IMSVidStreamBufferSource2.get_WSTCounter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferSource2::get_WSTCounter


## -description



The <b>get_WSTCounter</b> method enables the caller to get performance statistics from the Stream Buffer Source for the World Standard Teletext (WST) stream.




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




<a href="https://msdn.microsoft.com/47012868-4c9e-4974-8549-11331836bed0">IMSVidStreamBufferSource2 Interface</a>
 

 

