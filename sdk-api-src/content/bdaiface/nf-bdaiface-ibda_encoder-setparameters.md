---
UID: NF:bdaiface.IBDA_Encoder.SetParameters
title: IBDA_Encoder::SetParameters
author: windows-sdk-content
description: Sets the parameters for the Encoder Service.
old-location: mstv\ibda_encoder_setparameters.htm
old-project: mstv
ms.assetid: 0ee90121-b52b-47dc-b954-e7ba0b14f75c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_Encoder interface [Microsoft TV Technologies],SetParameters method, IBDA_Encoder.SetParameters, IBDA_Encoder::SetParameters, PBDA_Encoder_BitrateMode_Average, PBDA_Encoder_BitrateMode_Constant, PBDA_Encoder_BitrateMode_Variable, SetParameters, SetParameters method [Microsoft TV Technologies], SetParameters method [Microsoft TV Technologies],IBDA_Encoder interface, bdaiface/IBDA_Encoder::SetParameters, mstv.ibda_encoder_setparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Encoder.SetParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_Encoder::SetParameters


## -description


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/43ed9d91-c769-4fb3-bcd9-e5239ec5d9c7">IBDA_Encoder</a>
 

 

