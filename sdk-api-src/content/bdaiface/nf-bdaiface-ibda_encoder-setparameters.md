---
UID: NF:bdaiface.IBDA_Encoder.SetParameters
title: IBDA_Encoder::SetParameters (bdaiface.h)
description: Sets the parameters for the Encoder Service.
helpviewer_keywords: ["IBDA_Encoder interface [Microsoft TV Technologies]","SetParameters method","IBDA_Encoder.SetParameters","IBDA_Encoder::SetParameters","PBDA_Encoder_BitrateMode_Average","PBDA_Encoder_BitrateMode_Constant","PBDA_Encoder_BitrateMode_Variable","SetParameters","SetParameters method [Microsoft TV Technologies]","SetParameters method [Microsoft TV Technologies]","IBDA_Encoder interface","bdaiface/IBDA_Encoder::SetParameters","mstv.ibda_encoder_setparameters"]
old-location: mstv\ibda_encoder_setparameters.htm
tech.root: mstv
ms.assetid: 0ee90121-b52b-47dc-b954-e7ba0b14f75c
ms.date: 12/05/2018
ms.keywords: IBDA_Encoder interface [Microsoft TV Technologies],SetParameters method, IBDA_Encoder.SetParameters, IBDA_Encoder::SetParameters, PBDA_Encoder_BitrateMode_Average, PBDA_Encoder_BitrateMode_Constant, PBDA_Encoder_BitrateMode_Variable, SetParameters, SetParameters method [Microsoft TV Technologies], SetParameters method [Microsoft TV Technologies],IBDA_Encoder interface, bdaiface/IBDA_Encoder::SetParameters, mstv.ibda_encoder_setparameters
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_Encoder::SetParameters
 - bdaiface/IBDA_Encoder::SetParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Encoder.SetParameters
---

# IBDA_Encoder::SetParameters


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sets the parameters for the Encoder Service.

## -parameters

### -param AudioBitrateMode [in]

The audio compression mode. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_BitrateMode_Constant"></a><a id="pbda_encoder_bitratemode_constant"></a><a id="PBDA_ENCODER_BITRATEMODE_CONSTANT"></a><dl>
<dt><b>PBDA_Encoder_BitrateMode_Constant</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Constant bit rate (CBR) mode.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_BitrateMode_Variable"></a><a id="pbda_encoder_bitratemode_variable"></a><a id="PBDA_ENCODER_BITRATEMODE_VARIABLE"></a><dl>
<dt><b>PBDA_Encoder_BitrateMode_Variable</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Variable bit rate (VBR) mode.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_BitrateMode_Average"></a><a id="pbda_encoder_bitratemode_average"></a><a id="PBDA_ENCODER_BITRATEMODE_AVERAGE"></a><dl>
<dt><b>PBDA_Encoder_BitrateMode_Average</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Average bit rate (ABR) mode.

</td>
</tr>
</table>

### -param AudioBitrate [in]

The audio bit rate.

### -param AudioMethodID [in]

The active audio encoder method.

### -param AudioProgram [in]

The audio program number.

### -param VideoBitrateMode [in]

The video compression mode. For a list of values, see <i>AudioBitrateMode</i>.

### -param VideoBitrate [in]

The video bit rate.

### -param VideoMethodID [in]

The active video encoder method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_encoder">IBDA_Encoder</a>