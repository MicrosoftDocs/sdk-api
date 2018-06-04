---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

