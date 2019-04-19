---
UID: NF:segment.IMSVidStreamBufferSink3.get_WSTCounter
title: IMSVidStreamBufferSink3::get_WSTCounter (segment.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersink3_get_wstcounter.htm
tech.root: mstv
ms.assetid: 4698bcce-e3df-4631-a363-0b3d54f8e38a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],get_WSTCounter method, IMSVidStreamBufferSink3.get_WSTCounter, IMSVidStreamBufferSink3::get_WSTCounter, IMSVidStreamBufferSink3get_WSTCounter, get_WSTCounter, get_WSTCounter method [Microsoft TV Technologies], get_WSTCounter method [Microsoft TV Technologies],IMSVidStreamBufferSink3 interface, mstv.imsvidstreambuffersink3_get_wstcounter, segment/IMSVidStreamBufferSink3::get_WSTCounter
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
 - IMSVidStreamBufferSink3.get_WSTCounter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSink3::get_WSTCounter


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_WSTCounter</b> method enables the caller to get performance statistics from the Stream Buffer Sink for the World Standard Teletext (WST) stream.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd694627(v=VS.85).aspx">IMSVidStreamBufferSink3 Interface</a>
 

 

