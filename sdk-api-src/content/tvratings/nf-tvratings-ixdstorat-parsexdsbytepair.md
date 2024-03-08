---
UID: NF:tvratings.IXDSToRat.ParseXDSBytePair
title: IXDSToRat::ParseXDSBytePair (tvratings.h)
description: .
helpviewer_keywords: ["IXDSToRat interface [Microsoft TV Technologies]","ParseXDSBytePair method","IXDSToRat.ParseXDSBytePair","IXDSToRat::ParseXDSBytePair","IXDSToRatParseXDSBytePair","ParseXDSBytePair","ParseXDSBytePair method [Microsoft TV Technologies]","ParseXDSBytePair method [Microsoft TV Technologies]","IXDSToRat interface","mstv.ixdstorat_parsexdsbytepair","tvratings/IXDSToRat::ParseXDSBytePair"]
old-location: mstv\ixdstorat_parsexdsbytepair.htm
tech.root: mstv
ms.assetid: 79c83962-13ac-4604-a6f0-677ea6f4af84
ms.date: 12/05/2018
ms.keywords: IXDSToRat interface [Microsoft TV Technologies],ParseXDSBytePair method, IXDSToRat.ParseXDSBytePair, IXDSToRat::ParseXDSBytePair, IXDSToRatParseXDSBytePair, ParseXDSBytePair, ParseXDSBytePair method [Microsoft TV Technologies], ParseXDSBytePair method [Microsoft TV Technologies],IXDSToRat interface, mstv.ixdstorat_parsexdsbytepair, tvratings/IXDSToRat::ParseXDSBytePair
req.header: tvratings.h
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
 - IXDSToRat::ParseXDSBytePair
 - tvratings/IXDSToRat::ParseXDSBytePair
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tvratings.h
api_name:
 - IXDSToRat.ParseXDSBytePair
---

# IXDSToRat::ParseXDSBytePair


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ParseXDSBytePair</b> method parses a single byte pair from an XDS stream. If the byte pair is the last pair in a completed ratings packet, the method returns the rating information.

## -parameters

### -param byte1 [in]

The first byte of the byte pair.

### -param byte2 [in]

The second byte of the byte pair.

### -param pEnSystem [out]

Receives the rating system, as a member of the <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration type.

### -param pEnLevel [out]

Receives the rating level, as a member of the <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.

### -param plBfEnAttributes [out]

Receives a bitwise combination of zero or more flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration. These flags specify additional content attributes, such as violence or adult language. They do not apply to every rating system.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No rating has been detected in the stream yet.

</td>
</tr>
</table>

## -remarks

The XDS Codec filter calls this method to pass XDS data to the <b>XDSToRat</b> object, one pair of bytes at a time. The <b>XDSToRat</b> object must store enough information between calls to be able to parse a complete ratings packet.

This method returns S_FALSE until the <b>XDSToRat</b> object decodes a complete ratings packet. At that point, the method returns S_OK and returns the rating information in the <i>pEnSystem</i>, <i>pEnLevel</i>, and <i>plBfEnAttributes</i> parameters. Subsequent calls return S_FALSE again until the next packet is decoded.

Ratings values may be delivered by either the XDS Content Advisory packet, or the Composite Packet-1 packet. For details, see sections 9.5.1.5 and 9.5.1.10, respectively, of the EIA/CEA-608B specification.

This method should also detect the Current Class Program Identification Number and Program Name packets indicating the end of show and return an S_OK value along with the values in the following table.

Return the following values for non-ratings packets.

<table>
<tr>
<th>Parameter
            </th>
<th>Value
            </th>
</tr>
<tr>
<td><i>pEnSystem</i></td>
<td><b>TvRat-SystemDontKnow</b></td>
</tr>
<tr>
<td><i>pEnLevel</i></td>
<td><b>TvRat_LevelDontKnow</b></td>
</tr>
<tr>
<td><i>plBfEnAttributes</i></td>
<td><b>BfAttrNone</b></td>
</tr>
</table>
 

For details, see section 9.5.1.5.4 (General Content Advisory Requirements) of the EIA/CEA-608-B specification.

## -see-also

<a href="/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ixdstorat">IXDSToRat Interface</a>