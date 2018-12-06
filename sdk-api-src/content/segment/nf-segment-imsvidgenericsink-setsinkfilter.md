---
UID: NF:segment.IMSVidGenericSink.SetSinkFilter
title: IMSVidGenericSink::SetSinkFilter
author: windows-sdk-content
description: The SetSinkFilter method sets the filter for the sink.
old-location: mstv\imsvidgenericsink_setsinkfilter.htm
tech.root: mstv
ms.assetid: 51a26dc5-a551-4f97-9dd4-6522a14989a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidGenericSink interface [Microsoft TV Technologies],SetSinkFilter method, IMSVidGenericSink.SetSinkFilter, IMSVidGenericSink::SetSinkFilter, IMSVidGenericSinkSetSinkFilter, SetSinkFilter, SetSinkFilter method [Microsoft TV Technologies], SetSinkFilter method [Microsoft TV Technologies],IMSVidGenericSink interface, mstv.imsvidgenericsink_setsinkfilter, segment/IMSVidGenericSink::SetSinkFilter
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
 - IMSVidGenericSink.SetSinkFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidGenericSink::SetSinkFilter


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        </div>
<div> </div>


The <b>SetSinkFilter</b> method sets the filter for the sink.


## -parameters




### -param bstrName [in]

<b>BSTR</b> that contains the CLSID of the sink filter. The <b>BSTR</b> must use the following format: <code>{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</code>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/15181a89-aa64-4ecf-aaf5-4aac36753ddf">IMSVidGenericSink Interface</a>
 

 

