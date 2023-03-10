---
UID: NF:wmcontainer.IMFASFSplitter.Initialize
title: IMFASFSplitter::Initialize (wmcontainer.h)
description: Resets the Advanced Systems Format (ASF) splitter and configures it to parse data from an ASF data section.
helpviewer_keywords: ["IMFASFSplitter interface [Media Foundation]","Initialize method","IMFASFSplitter.Initialize","IMFASFSplitter::Initialize","Initialize","Initialize method [Media Foundation]","Initialize method [Media Foundation]","IMFASFSplitter interface","dd69c2f9-dabf-4bba-bb3b-75ec3208c189","mf.imfasfsplitter_initialize","wmcontainer/IMFASFSplitter::Initialize"]
old-location: mf\imfasfsplitter_initialize.htm
tech.root: mf
ms.assetid: dd69c2f9-dabf-4bba-bb3b-75ec3208c189
ms.date: 12/05/2018
ms.keywords: IMFASFSplitter interface [Media Foundation],Initialize method, IMFASFSplitter.Initialize, IMFASFSplitter::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFASFSplitter interface, dd69c2f9-dabf-4bba-bb3b-75ec3208c189, mf.imfasfsplitter_initialize, wmcontainer/IMFASFSplitter::Initialize
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
 - IMFASFSplitter::Initialize
 - wmcontainer/IMFASFSplitter::Initialize
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
 - IMFASFSplitter.Initialize
---

# IMFASFSplitter::Initialize


## -description

Resets the Advanced Systems Format (ASF) splitter and configures it to parse data from an ASF data section.

## -parameters

### -param pIContentInfo [in]

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface of a ContentInfo object that describes the data to be parsed.

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
The <i>pIContentInfo</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>