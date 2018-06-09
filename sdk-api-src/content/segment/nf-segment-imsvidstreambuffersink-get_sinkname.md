---
UID: NF:segment.IMSVidStreamBufferSink.get_SinkName
title: IMSVidStreamBufferSink::get_SinkName
author: windows-sdk-content
description: The get_SinkName method retrieves the name of the stub file that points to the backing files.
old-location: mstv\imsvidstreambuffersink_get_sinkname.htm
old-project: mstv
ms.assetid: a1fda0a0-7b18-4eb8-9555-19fb92fc32f2
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],get_SinkName method, IMSVidStreamBufferSink.get_SinkName, IMSVidStreamBufferSink::get_SinkName, IMSVidStreamBufferSinkget_SinkName, get_SinkName, get_SinkName method [Microsoft TV Technologies], get_SinkName method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, mstv.imsvidstreambuffersink_get_sinkname, segment/IMSVidStreamBufferSink::get_SinkName
ms.prod: windows
ms.technology: windows-sdk
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
 - IMSVidStreamBufferSink.get_SinkName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSink::get_SinkName


## -description


The <b>get_SinkName</b> method retrieves the name of the stub file that points to the backing files.


## -parameters




### -param pName [out]

Pointer to a variable that receives the file name.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

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



The caller must release the returned string, using the <b>SysFreeString</b> function.




## -see-also




<a href="https://msdn.microsoft.com/cc0490ac-bc0d-472c-b0a7-5e0f81054921">Buffering in the Stream Buffer Engine</a>



<a href="https://msdn.microsoft.com/80f6cd3a-8cb8-4bda-9b66-33e7d214015a">IMSVidStreamBufferSink Interface</a>
 

 

