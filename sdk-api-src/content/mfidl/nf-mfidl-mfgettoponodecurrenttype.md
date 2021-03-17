---
UID: NF:mfidl.MFGetTopoNodeCurrentType
title: MFGetTopoNodeCurrentType function (mfidl.h)
description: Gets the media type for a stream associated with a topology node.
helpviewer_keywords: ["MFGetTopoNodeCurrentType","MFGetTopoNodeCurrentType function [Media Foundation]","mf.mfgettoponodecurrenttype","mfidl/MFGetTopoNodeCurrentType"]
old-location: mf\mfgettoponodecurrenttype.htm
tech.root: mf
ms.assetid: 2405c6f6-1a3c-42d1-8ec9-4728f522ce42
ms.date: 12/05/2018
ms.keywords: MFGetTopoNodeCurrentType, MFGetTopoNodeCurrentType function [Media Foundation], mf.mfgettoponodecurrenttype, mfidl/MFGetTopoNodeCurrentType
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetTopoNodeCurrentType
 - mfidl/MFGetTopoNodeCurrentType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFGetTopoNodeCurrentType
---

# MFGetTopoNodeCurrentType function


## -description

Gets the media type for a stream associated with a topology node.

## -parameters

### -param pNode

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface.

### -param dwStreamIndex

The identifier of the stream to query. This parameter is interpreted as follows:

<ul>
<li>Transform nodes: The value is the zero-based index of the input or output stream.</li>
<li>All other node types: The value must be zero.</li>
</ul>

### -param fOutput

<b>If TRUE</b>, the function gets an output type<b>. If FALSE</b>, the function gets an input type. This parameter is interpreted as follows:

<ul>
<li>Output nodes: The value must be <b>TRUE</b>.</li>
<li>Source nodes: The value must be <b>FALSE</b>.</li>
<li>Tee nodes: The value is ignored.</li>
<li>Transform nodes: If the value is <b>TRUE</b>, the <i>dwStreamIndex</i> parameter is the index for an output stream. Otherwise, <i>dwStreamIndex</i> is the index for an input stream.</li>
</ul>

### -param ppType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The stream index is invalid.

</td>
</tr>
</table>

## -remarks

This function gets the actual media type from the object that is associated with the topology node. The <i>pNode</i> parameter should specify a node that belongs to a fully resolved topology.  If the node belongs to a partial topology, the function will probably fail. 

Tee nodes do not have an associated object to query. For tee nodes, the function gets the node's input type, if available. Otherwise, if no input type is available, the function gets the media type of the node's primary output stream. The primary output stream is identified by the <a href="/windows/desktop/medfound/mf-toponode-primaryoutput-attribute">MF_TOPONODE_PRIMARYOUTPUT</a>  attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>