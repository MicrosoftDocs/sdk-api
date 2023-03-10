---
UID: NF:wmcontainer.IMFASFSplitter.GetNextSample
title: IMFASFSplitter::GetNextSample (wmcontainer.h)
description: Retrieves a sample from the Advanced Systems Format (ASF) splitter after the data has been parsed.
helpviewer_keywords: ["85133059-6710-4fb2-b42b-f54747816f9c","ASF_STATUSFLAGS_INCOMPLETE","GetNextSample","GetNextSample method [Media Foundation]","GetNextSample method [Media Foundation]","IMFASFSplitter interface","IMFASFSplitter interface [Media Foundation]","GetNextSample method","IMFASFSplitter.GetNextSample","IMFASFSplitter::GetNextSample","Zero","mf.imfasfsplitter_getnextsample","wmcontainer/IMFASFSplitter::GetNextSample"]
old-location: mf\imfasfsplitter_getnextsample.htm
tech.root: mf
ms.assetid: 85133059-6710-4fb2-b42b-f54747816f9c
ms.date: 12/05/2018
ms.keywords: 85133059-6710-4fb2-b42b-f54747816f9c, ASF_STATUSFLAGS_INCOMPLETE, GetNextSample, GetNextSample method [Media Foundation], GetNextSample method [Media Foundation],IMFASFSplitter interface, IMFASFSplitter interface [Media Foundation],GetNextSample method, IMFASFSplitter.GetNextSample, IMFASFSplitter::GetNextSample, Zero, mf.imfasfsplitter_getnextsample, wmcontainer/IMFASFSplitter::GetNextSample
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFSplitter::GetNextSample
 - wmcontainer/IMFASFSplitter::GetNextSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter.GetNextSample
---

# IMFASFSplitter::GetNextSample


## -description

Retrieves a sample from the Advanced Systems Format (ASF) splitter after the data has been parsed.

## -parameters

### -param pdwStatusFlags [out]

Receives one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ASF_STATUSFLAGS_INCOMPLETE"></a><a id="asf_statusflags_incomplete"></a><dl>
<dt><b>ASF_STATUSFLAGS_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
More samples are ready to be retrieved. Call <b>GetNextSample</b> in a loop until the <i>pdwStatusFlags</i> parameter receives the value zero.

</td>
</tr>
<tr>
<td width="40%"><a id="Zero"></a><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
No additional samples are ready. Call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata">IMFASFSplitter::ParseData</a> to give more input data to the splitter.

</td>
</tr>
</table>

### -param pwStreamNumber [out]

If the method returns a sample in the <i>ppISample</i> parameter, this parameter receives the number of the stream to which the sample belongs.

### -param ppISample [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the parsed sample. The caller must release the interface. If no samples are ready, this parameter receives the value <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
The ASF data in the buffer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ASF_MISSINGDATA</b></dt>
</dl>
</td>
<td width="60%">
There is a gap in the ASF data.

</td>
</tr>
</table>

## -remarks

Before calling this method, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata">IMFASFSplitter::ParseData</a> to give input data to the splitter. If the input does not contain enough data for a complete sample, the <b>GetNextSample</b> method succeeds but returns <b>NULL</b> in the <i>ppISample</i> parameter.

The ASF splitter skips samples for unselected streams. To select streams, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams">IMFASFSplitter::SelectStreams</a>.

## -see-also

<a href="/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>