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

# AEC_VAD_MODE enumeration


## -description


Specifies the type of voice activity detection (VAD) for the voice capture DSP. This enumeration is used with the <a href="https://msdn.microsoft.com/59c8e348-8c08-4cf8-9c72-8d0f4fabc473">MFPKEY_WMAAECMA_FEATR_VAD</a> property.


## -enum-fields




### -field AEC_VAD_DISABLED

Voice activity detection is disabled.


### -field AEC_VAD_NORMAL

General purpose VAD. This setting attempts to balance the false detection rate and the missed detection rate. The output can have the following values.
	     

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Non-speech.</td>
</tr>
<tr>
<td>1</td>
<td>Voiced speech.</td>
</tr>
<tr>
<td>2</td>
<td>Unvoiced speech.</td>
</tr>
<tr>
<td>3</td>
<td>Mixture of voiced and unvoiced speech.</td>
</tr>
</table>
 


### -field AEC_VAD_FOR_AGC

Voice activity detection for automatic gain control and noise suppression. In this mode, the VAD threshold is higher than the normal mode, to reduce the false detection rate. The output distinguishes voiced speech from other sounds (non-speech or unvoiced speech). The output can have the following values.
        

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Non-speech or unvoiced speech.</td>
</tr>
<tr>
<td>1</td>
<td>Voiced speech.</td>
</tr>
</table>
 


### -field AEC_VAD_FOR_SILENCE_SUPPRESSION

Voice activity detection for silence suppression. In this mode, the output distinguishes speech (voiced or unvoiced) from non-speech. The output can have the following values.
        

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Non-speech.</td>
</tr>
<tr>
<td>1</td>
<td>Voiced or unvoiced speech.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/6c77c8f6-289e-4130-b56a-e1f0bcc40f3e">Voice Capture</a>
 

 

