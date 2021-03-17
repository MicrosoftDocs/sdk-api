---
UID: NF:wmcontainer.IMFASFSplitter.SelectStreams
title: IMFASFSplitter::SelectStreams (wmcontainer.h)
description: Sets the streams to be parsed by the Advanced Systems Format (ASF) splitter.
helpviewer_keywords: ["IMFASFSplitter interface [Media Foundation]","SelectStreams method","IMFASFSplitter.SelectStreams","IMFASFSplitter::SelectStreams","SelectStreams","SelectStreams method [Media Foundation]","SelectStreams method [Media Foundation]","IMFASFSplitter interface","a241f8a4-7609-4a6c-825f-a7b882bfc25f","mf.imfasfsplitter_selectstreams","wmcontainer/IMFASFSplitter::SelectStreams"]
old-location: mf\imfasfsplitter_selectstreams.htm
tech.root: mf
ms.assetid: a241f8a4-7609-4a6c-825f-a7b882bfc25f
ms.date: 12/05/2018
ms.keywords: IMFASFSplitter interface [Media Foundation],SelectStreams method, IMFASFSplitter.SelectStreams, IMFASFSplitter::SelectStreams, SelectStreams, SelectStreams method [Media Foundation], SelectStreams method [Media Foundation],IMFASFSplitter interface, a241f8a4-7609-4a6c-825f-a7b882bfc25f, mf.imfasfsplitter_selectstreams, wmcontainer/IMFASFSplitter::SelectStreams
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
 - IMFASFSplitter::SelectStreams
 - wmcontainer/IMFASFSplitter::SelectStreams
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
 - IMFASFSplitter.SelectStreams
---

# IMFASFSplitter::SelectStreams


## -description

Sets the streams to be parsed by the Advanced Systems Format (ASF) splitter.

## -parameters

### -param pwStreamNumbers [in]

An array of variables containing the list of stream numbers to select.

### -param wNumStreams [in]

The number of valid elements in the stream number array.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwStreamNumbers</i> is <b>NULL</b> and <i>wNumStreams</i> contains a value greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number was passed in the array.

</td>
</tr>
</table>

## -remarks

Calling this method supersedes any previous stream selections; only the streams specified in the <i>pwStreamNumbers</i> array will be selected.

By default, no streams are selected by the splitter.

You can obtain a list of the currently selected streams by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams">IMFASFSplitter::GetSelectedStreams</a> method.

## -see-also

<a href="/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>