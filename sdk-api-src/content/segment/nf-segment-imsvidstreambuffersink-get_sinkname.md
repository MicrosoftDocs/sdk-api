---
UID: NF:segment.IMSVidStreamBufferSink.get_SinkName
title: IMSVidStreamBufferSink::get_SinkName (segment.h)
description: The get_SinkName method retrieves the name of the stub file that points to the backing files.
helpviewer_keywords: ["IMSVidStreamBufferSink interface [Microsoft TV Technologies]","get_SinkName method","IMSVidStreamBufferSink.get_SinkName","IMSVidStreamBufferSink::get_SinkName","IMSVidStreamBufferSinkget_SinkName","get_SinkName","get_SinkName method [Microsoft TV Technologies]","get_SinkName method [Microsoft TV Technologies]","IMSVidStreamBufferSink interface","mstv.imsvidstreambuffersink_get_sinkname","segment/IMSVidStreamBufferSink::get_SinkName"]
old-location: mstv\imsvidstreambuffersink_get_sinkname.htm
tech.root: mstv
ms.assetid: a1fda0a0-7b18-4eb8-9555-19fb92fc32f2
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],get_SinkName method, IMSVidStreamBufferSink.get_SinkName, IMSVidStreamBufferSink::get_SinkName, IMSVidStreamBufferSinkget_SinkName, get_SinkName, get_SinkName method [Microsoft TV Technologies], get_SinkName method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, mstv.imsvidstreambuffersink_get_sinkname, segment/IMSVidStreamBufferSink::get_SinkName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSink::get_SinkName
 - segment/IMSVidStreamBufferSink::get_SinkName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSink.get_SinkName
---

# IMSVidStreamBufferSink::get_SinkName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

<a href="/previous-versions/windows/desktop/mstv/buffering-in-the-stream-buffer-engine">Buffering in the Stream Buffer Engine</a>



<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersink">IMSVidStreamBufferSink Interface</a>