---
UID: NF:encdec.IXDSCodec.GetContentAdvisoryRating
title: IXDSCodec::GetContentAdvisoryRating (encdec.h)
description: The GetContentAdvisoryRating method retrieves the most recent ratings information parsed by the XDSToRat object.
helpviewer_keywords: ["GetContentAdvisoryRating","GetContentAdvisoryRating method [Microsoft TV Technologies]","GetContentAdvisoryRating method [Microsoft TV Technologies]","IXDSCodec interface","IXDSCodec interface [Microsoft TV Technologies]","GetContentAdvisoryRating method","IXDSCodec.GetContentAdvisoryRating","IXDSCodec::GetContentAdvisoryRating","IXDSCodecGetContentAdvisoryRating","encdec/IXDSCodec::GetContentAdvisoryRating","mstv.ixdscodec_getcontentadvisoryrating"]
old-location: mstv\ixdscodec_getcontentadvisoryrating.htm
tech.root: mstv
ms.assetid: 725e444c-ecf4-49da-a800-cc3faf627eea
ms.date: 12/05/2018
ms.keywords: GetContentAdvisoryRating, GetContentAdvisoryRating method [Microsoft TV Technologies], GetContentAdvisoryRating method [Microsoft TV Technologies],IXDSCodec interface, IXDSCodec interface [Microsoft TV Technologies],GetContentAdvisoryRating method, IXDSCodec.GetContentAdvisoryRating, IXDSCodec::GetContentAdvisoryRating, IXDSCodecGetContentAdvisoryRating, encdec/IXDSCodec::GetContentAdvisoryRating, mstv.ixdscodec_getcontentadvisoryrating
f1_keywords:
- encdec/IXDSCodec.GetContentAdvisoryRating
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- EncDec.h
api_name:
- IXDSCodec.GetContentAdvisoryRating
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXDSCodec::GetContentAdvisoryRating


## -description


The <b>GetContentAdvisoryRating</b> method retrieves the most recent ratings information parsed by the <b>XDSToRat</b> object.


## -parameters




### -param pRat [out]

Receives the most recent rating. The rating is packed into a format that is used internally by the XDS Codec filter, Encrypter/Tagger filter, and Decrypter/Detagger filter. It is not intended for use by other objects.


### -param pPktSeqID [out]

Receives the number of ratings packets that have been decoded. This information can be used for diagnostic purposes.


### -param pCallSeqID [out]

Receives the number of times this method has been called for the current ratings packet. This information can be used for diagnostic purposes.


### -param pTimeStart [out]

Receives the start time of the sample that completed the ratings packet.


### -param pTimeEnd [out]

Receives the stop time of the sample that completed the ratings packet.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-ixdscodec">IXDSCodec Interface</a>
 

 

