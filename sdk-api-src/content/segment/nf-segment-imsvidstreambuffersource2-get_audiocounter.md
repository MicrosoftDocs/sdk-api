---
UID: NF:segment.IMSVidStreamBufferSource2.get_AudioCounter
title: IMSVidStreamBufferSource2::get_AudioCounter
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersource2_get_audiocounter.htm
old-project: mstv
ms.assetid: 310e59e1-afde-45ed-b2d1-eecf59319935
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidStreamBufferSource2 interface [Microsoft TV Technologies],get_AudioCounter method, IMSVidStreamBufferSource2.get_AudioCounter, IMSVidStreamBufferSource2::get_AudioCounter, IMSVidStreamBufferSource2get_AudioCounter, get_AudioCounter, get_AudioCounter method [Microsoft TV Technologies], get_AudioCounter method [Microsoft TV Technologies],IMSVidStreamBufferSource2 interface, mstv.imsvidstreambuffersource2_get_audiocounter, segment/IMSVidStreamBufferSource2::get_AudioCounter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSource2.get_AudioCounter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSource2::get_AudioCounter


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_AudioCounter</b> method enables the caller to get performance statistics from the Stream Buffer Source for the audio stream.


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



<a href="https://msdn.microsoft.com/9def9b51-bae7-49a2-b32f-61811be63c58">get_VideoCounter</a>
 

 

