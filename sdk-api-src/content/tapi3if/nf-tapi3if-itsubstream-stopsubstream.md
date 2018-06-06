---
UID: NF:tapi3if.ITSubStream.StopSubStream
title: ITSubStream::StopSubStream
author: windows-sdk-content
description: The StopSubStream method stops the substream. For additional information, see ITStream::StopStream.
old-location: tapi3\itsubstream_stopsubstream.htm
old-project: Tapi
ms.assetid: fa5028f6-80eb-4076-a81c-c83b462fc27c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITSubStream interface [TAPI 2.2],StopSubStream method, ITSubStream.StopSubStream, ITSubStream::StopSubStream, StopSubStream, StopSubStream method [TAPI 2.2], StopSubStream method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_stopsubstream, tapi3.itsubstream_stopsubstream, tapi3if/ITSubStream::StopSubStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITSubStream.StopSubStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSubStream::StopSubStream


## -description


The 
<b>StopSubStream</b> method stops the substream. For additional information, see 
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">ITStream::StopStream</a>.


## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support this operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

