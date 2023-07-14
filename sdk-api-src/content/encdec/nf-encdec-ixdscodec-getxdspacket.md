---
UID: NF:encdec.IXDSCodec.GetXDSPacket
title: IXDSCodec::GetXDSPacket (encdec.h)
description: The GetXDSPacket method retrieves the most recent XDS packet.
helpviewer_keywords: ["GetXDSPacket","GetXDSPacket method [Microsoft TV Technologies]","GetXDSPacket method [Microsoft TV Technologies]","IXDSCodec interface","IXDSCodec interface [Microsoft TV Technologies]","GetXDSPacket method","IXDSCodec.GetXDSPacket","IXDSCodec::GetXDSPacket","IXDSCodecGetXDSPacket","encdec/IXDSCodec::GetXDSPacket","mstv.ixdscodec_getxdspacket"]
old-location: mstv\ixdscodec_getxdspacket.htm
tech.root: mstv
ms.assetid: 44a74489-4ed7-42f0-b8d5-bf86e0f7072c
ms.date: 12/05/2018
ms.keywords: GetXDSPacket, GetXDSPacket method [Microsoft TV Technologies], GetXDSPacket method [Microsoft TV Technologies],IXDSCodec interface, IXDSCodec interface [Microsoft TV Technologies],GetXDSPacket method, IXDSCodec.GetXDSPacket, IXDSCodec::GetXDSPacket, IXDSCodecGetXDSPacket, encdec/IXDSCodec::GetXDSPacket, mstv.ixdscodec_getxdspacket
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
 - IXDSCodec::GetXDSPacket
 - encdec/IXDSCodec::GetXDSPacket
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
 - IXDSCodec.GetXDSPacket
---

# IXDSCodec::GetXDSPacket


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetXDSPacket</b> method retrieves the most recent XDS packet.

## -parameters

### -param pXDSClassPkt [out]

Receives the packet class.

### -param pXDSTypePkt [out]

Receives the class-specific packet type.

### -param pBstrXDSPkt [out]

Receives the packet as a <b>BSTR</b> value.

### -param pPktSeqID [out]

Receives the number of ratings packets that have been decoded. This information can be used for diagnostic purposes.

### -param pCallSeqID [out]

Receives the number of times this method has been called for the current ratings packet. This information can be used for diagnostic purposes.

### -param pTimeStart [out]

Receives the start time of the sample containing the packet.

### -param pTimeEnd [out]

Receives the stop time of the sample containing the packet.

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
<b>NULL</b> pointer argument

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

## -remarks

The returned <b>BSTR</b> contains binary data which might include embedded NULL characters. The caller must free the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ixdscodec">IXDSCodec Interface</a>