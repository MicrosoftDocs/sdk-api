---
UID: NF:encdec.IXDSCodec.put_CCSubstreamService
title: IXDSCodec::put_CCSubstreamService (encdec.h)
description: The put_CCSubstreamService method specifies which line 21 data channels the XDS Codec filter sends to the XDSToRat object. By default, only the Extended Data Services (XDS) channel is supported.
helpviewer_keywords: ["IXDSCodec interface [Microsoft TV Technologies]","put_CCSubstreamService method","IXDSCodec.put_CCSubstreamService","IXDSCodec::put_CCSubstreamService","IXDSCodecput_CCSubstreamService","encdec/IXDSCodec::put_CCSubstreamService","mstv.ixdscodec_put_ccsubstreamservice","put_CCSubstreamService","put_CCSubstreamService method [Microsoft TV Technologies]","put_CCSubstreamService method [Microsoft TV Technologies]","IXDSCodec interface"]
old-location: mstv\ixdscodec_put_ccsubstreamservice.htm
tech.root: mstv
ms.assetid: e8e4a43a-3e9f-468a-8df3-7ff05d23b20b
ms.date: 12/05/2018
ms.keywords: IXDSCodec interface [Microsoft TV Technologies],put_CCSubstreamService method, IXDSCodec.put_CCSubstreamService, IXDSCodec::put_CCSubstreamService, IXDSCodecput_CCSubstreamService, encdec/IXDSCodec::put_CCSubstreamService, mstv.ixdscodec_put_ccsubstreamservice, put_CCSubstreamService, put_CCSubstreamService method [Microsoft TV Technologies], put_CCSubstreamService method [Microsoft TV Technologies],IXDSCodec interface
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IXDSCodec::put_CCSubstreamService
 - encdec/IXDSCodec::put_CCSubstreamService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IXDSCodec.put_CCSubstreamService
---

# IXDSCodec::put_CCSubstreamService


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_CCSubstreamService</b> method specifies which line 21 data channels the XDS Codec filter sends to the <b>XDSToRat</b> object. By default, only the Extended Data Services (XDS) channel is supported.

## -parameters

### -param SubstreamMask [in]

Bitwise combination of zero or more <a href="/previous-versions/windows/desktop/mstv/ks-cc-substream">KS_CC_SUBSTREAM</a> flags, specifying the line 21 services.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ixdscodec">IXDSCodec Interface</a>