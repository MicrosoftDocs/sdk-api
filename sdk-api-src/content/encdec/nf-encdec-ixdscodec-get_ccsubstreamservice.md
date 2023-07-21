---
UID: NF:encdec.IXDSCodec.get_CCSubstreamService
title: IXDSCodec::get_CCSubstreamService (encdec.h)
description: The get_CCSubstreamService method queries which line 21 data channels the XDS Codec filter sends to the XDSToRat object. By default, it sends just the Extended Data Services (XDS) channel.
helpviewer_keywords: ["IXDSCodec interface [Microsoft TV Technologies]","get_CCSubstreamService method","IXDSCodec.get_CCSubstreamService","IXDSCodec::get_CCSubstreamService","IXDSCodecget_CCSubstreamService","encdec/IXDSCodec::get_CCSubstreamService","get_CCSubstreamService","get_CCSubstreamService method [Microsoft TV Technologies]","get_CCSubstreamService method [Microsoft TV Technologies]","IXDSCodec interface","mstv.ixdscodec_get_ccsubstreamservice"]
old-location: mstv\ixdscodec_get_ccsubstreamservice.htm
tech.root: mstv
ms.assetid: 60523c2c-0d57-46d7-8ab2-eaf065a440d4
ms.date: 12/05/2018
ms.keywords: IXDSCodec interface [Microsoft TV Technologies],get_CCSubstreamService method, IXDSCodec.get_CCSubstreamService, IXDSCodec::get_CCSubstreamService, IXDSCodecget_CCSubstreamService, encdec/IXDSCodec::get_CCSubstreamService, get_CCSubstreamService, get_CCSubstreamService method [Microsoft TV Technologies], get_CCSubstreamService method [Microsoft TV Technologies],IXDSCodec interface, mstv.ixdscodec_get_ccsubstreamservice
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
 - IXDSCodec::get_CCSubstreamService
 - encdec/IXDSCodec::get_CCSubstreamService
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
 - IXDSCodec.get_CCSubstreamService
---

# IXDSCodec::get_CCSubstreamService


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_CCSubstreamService</b> method queries which line 21 data channels the XDS Codec filter sends to the <b>XDSToRat</b> object. By default, it sends just the Extended Data Services (XDS) channel.

## -parameters

### -param pSubstreamMask [out, retval]

Receives a bitwise combination of zero or more <a href="/previous-versions/windows/desktop/mstv/ks-cc-substream">KS_CC_SUBSTREAM</a> flags.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
NULL pointer argument

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