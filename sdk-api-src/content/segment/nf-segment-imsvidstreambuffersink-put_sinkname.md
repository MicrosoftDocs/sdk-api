---
UID: NF:segment.IMSVidStreamBufferSink.put_SinkName
title: IMSVidStreamBufferSink::put_SinkName
author: windows-sdk-content
description: The put_SinkName method sets the name of the stub file that points to the backing files.
old-location: mstv\imsvidstreambuffersink_put_sinkname.htm
tech.root: mstv
ms.assetid: 5269ab81-0963-4a86-9592-d670cca6016f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],put_SinkName method, IMSVidStreamBufferSink.put_SinkName, IMSVidStreamBufferSink::put_SinkName, IMSVidStreamBufferSinkput_SinkName, mstv.imsvidstreambuffersink_put_sinkname, put_SinkName, put_SinkName method [Microsoft TV Technologies], put_SinkName method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, segment/IMSVidStreamBufferSink::put_SinkName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IMSVidStreamBufferSink.put_SinkName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSink::put_SinkName


## -description


The <b>put_SinkName</b> method sets the name of the stub file that points to the backing files.


## -parameters




### -param Name [in]

Specifies the file name.


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
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
 




## -remarks



Call this method before calling <a href="https://msdn.microsoft.com/0195d515-4018-4a96-9af9-566fcdeffaf7">NameSetLock</a>, while the graph is stopped. Otherwise, the method fails and returns E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/cc0490ac-bc0d-472c-b0a7-5e0f81054921">Buffering in the Stream Buffer Engine</a>



<a href="https://msdn.microsoft.com/80f6cd3a-8cb8-4bda-9b66-33e7d214015a">IMSVidStreamBufferSink Interface</a>
 

 

