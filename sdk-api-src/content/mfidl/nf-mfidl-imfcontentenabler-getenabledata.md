---
UID: NF:mfidl.IMFContentEnabler.GetEnableData
title: IMFContentEnabler::GetEnableData (mfidl.h)
description: Retrieves the data for a manual content enabling action.
helpviewer_keywords: ["GetEnableData","GetEnableData method [Media Foundation]","GetEnableData method [Media Foundation]","IMFContentEnabler interface","IMFContentEnabler interface [Media Foundation]","GetEnableData method","IMFContentEnabler.GetEnableData","IMFContentEnabler::GetEnableData","d1859037-7a33-4943-8ca9-6782fc8b0b92","mf.imfcontentenabler_getenabledata","mfidl/IMFContentEnabler::GetEnableData"]
old-location: mf\imfcontentenabler_getenabledata.htm
tech.root: mf
ms.assetid: d1859037-7a33-4943-8ca9-6782fc8b0b92
ms.date: 12/05/2018
ms.keywords: GetEnableData, GetEnableData method [Media Foundation], GetEnableData method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],GetEnableData method, IMFContentEnabler.GetEnableData, IMFContentEnabler::GetEnableData, d1859037-7a33-4943-8ca9-6782fc8b0b92, mf.imfcontentenabler_getenabledata, mfidl/IMFContentEnabler::GetEnableData
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFContentEnabler::GetEnableData
 - mfidl/IMFContentEnabler::GetEnableData
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
 - IMFContentEnabler.GetEnableData
---

# IMFContentEnabler::GetEnableData


## -description

Retrieves the data for a manual content enabling action.

## -parameters

### -param ppbData [out]

Receives a pointer to a buffer that contains the data. The caller must free the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbData [out]

Receives the size of the <i>ppbData</i> buffer.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No data is available.

</td>
</tr>
</table>

## -remarks

The purpose of the data depends on the content enabler type, which is obtained by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabletype">IMFContentEnabler::GetEnableType</a>.

<table>
<tr>
<th>Enable type</th>
<th>Purpose of data</th>
</tr>
<tr>
<td>Individualization</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>License acquisition</td>
<td>HTTP POST data.</td>
</tr>
<tr>
<td>Revocation</td>
<td>
<a href="/windows/desktop/api/mfidl/ns-mfidl-mfrr_components">MFRR_COMPONENTS</a> structure.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a>