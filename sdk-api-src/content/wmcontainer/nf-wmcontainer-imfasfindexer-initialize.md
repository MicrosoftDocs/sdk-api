---
UID: NF:wmcontainer.IMFASFIndexer.Initialize
title: IMFASFIndexer::Initialize (wmcontainer.h)
description: Initializes the indexer object.
helpviewer_keywords: ["IMFASFIndexer interface [Media Foundation]","Initialize method","IMFASFIndexer.Initialize","IMFASFIndexer::Initialize","Initialize","Initialize method [Media Foundation]","Initialize method [Media Foundation]","IMFASFIndexer interface","c02931d3-7b43-43a9-9e4e-00945ba3c8d8","mf.imfasfindexer_initialize","wmcontainer/IMFASFIndexer::Initialize"]
old-location: mf\imfasfindexer_initialize.htm
tech.root: mf
ms.assetid: c02931d3-7b43-43a9-9e4e-00945ba3c8d8
ms.date: 12/05/2018
ms.keywords: IMFASFIndexer interface [Media Foundation],Initialize method, IMFASFIndexer.Initialize, IMFASFIndexer::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFASFIndexer interface, c02931d3-7b43-43a9-9e4e-00945ba3c8d8, mf.imfasfindexer_initialize, wmcontainer/IMFASFIndexer::Initialize
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
 - IMFASFIndexer::Initialize
 - wmcontainer/IMFASFIndexer::Initialize
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
 - IMFASFIndexer.Initialize
---

# IMFASFIndexer::Initialize


## -description

Initializes the indexer object. This method reads information in a ContentInfo object about the configuration of the content and the properties of the existing index, if present. Use this method before using the indexer for either writing or reading an index. You must make this call before using any of the other methods of the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a> interface.

## -parameters

### -param pIContentInfo [in]

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface of the ContentInfo object describing the content with which to use the indexer.

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
Invalid ASF data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>

## -remarks

The indexer needs to examine the data in the ContentInfo object to properly write or read the index for the content. The indexer will not make changes to the content information and will not hold any references to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface.

In the ASF header, the maximum data-packet size must equal the minimum data-packet size. Otherwise, the method returns <b>MF_E_UNEXPECTED</b>.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>