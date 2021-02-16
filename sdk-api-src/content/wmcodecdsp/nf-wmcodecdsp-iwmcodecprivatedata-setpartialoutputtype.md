---
UID: NF:wmcodecdsp.IWMCodecPrivateData.SetPartialOutputType
title: IWMCodecPrivateData::SetPartialOutputType (wmcodecdsp.h)
description: Gives the codec the output media type without the codec data. This enables the codec to generate the private data.
helpviewer_keywords: ["IWMCodecPrivateData interface [Media Foundation]","SetPartialOutputType method","IWMCodecPrivateData.SetPartialOutputType","IWMCodecPrivateData::SetPartialOutputType","SetPartialOutputType","SetPartialOutputType method [Media Foundation]","SetPartialOutputType method [Media Foundation]","IWMCodecPrivateData interface","codecapi.iwmcodecprivatedatasetpartialoutputtype","mf.iwmcodecprivatedatasetpartialoutputtype","wmcodecdsp/IWMCodecPrivateData::SetPartialOutputType"]
old-location: mf\iwmcodecprivatedatasetpartialoutputtype.htm
tech.root: mf
ms.assetid: c906ac2d-b3e0-4ecd-8f0e-3fa1a2a0beea
ms.date: 12/05/2018
ms.keywords: IWMCodecPrivateData interface [Media Foundation],SetPartialOutputType method, IWMCodecPrivateData.SetPartialOutputType, IWMCodecPrivateData::SetPartialOutputType, SetPartialOutputType, SetPartialOutputType method [Media Foundation], SetPartialOutputType method [Media Foundation],IWMCodecPrivateData interface, codecapi.iwmcodecprivatedatasetpartialoutputtype, mf.iwmcodecprivatedatasetpartialoutputtype, wmcodecdsp/IWMCodecPrivateData::SetPartialOutputType
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IWMCodecPrivateData::SetPartialOutputType
 - wmcodecdsp/IWMCodecPrivateData::SetPartialOutputType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecPrivateData.SetPartialOutputType
---

# IWMCodecPrivateData::SetPartialOutputType


## -description

Gives the codec the output media type without the codec data. This enables the codec to generate the private data.

## -parameters

### -param pmt [in]

Address of the partial output media type.

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
</table>

## -remarks

The DMO_MEDIA_TYPE that you pass to this method is only partial in that it does not include the appended private data. It must be complete in all other ways.

If you are setting properties on an encoder, you must finish that configuration before getting the private data. Changing properties invalidates any private data previously retrieved. If you change properties after getting the private data, retrieve it again and reset the output type.

You must call this method before calling <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata">IWMCodecPrivateData::GetPrivateData</a> to get the private data.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata">IWMCodecPrivateData Interface</a>