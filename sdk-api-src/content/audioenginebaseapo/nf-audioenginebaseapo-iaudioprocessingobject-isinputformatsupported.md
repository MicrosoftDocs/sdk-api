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

# IAudioProcessingObject::IsInputFormatSupported


## -description


This method negotiates with the Windows Vista audio engine to establish a data format for the stream of audio data.


## -parameters




### -param pOppositeFormat [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536496">IAudioMediaType</a> interface. This parameter is used to indicate the output format of the data. The value of pOppositeFormat must be set to <b>NULL</b> to indicate that the output format can be any type.


### -param pRequestedInputFormat [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536496">IAudioMediaType</a> interface. This parameter is used to indicate the input format that is to be verified.


### -param ppSupportedInputFormat [out, optional]

This parameter indicates the supported format that is closest to the format to be verified.


## -returns



If the call completed successfully, the ppSupportedInputFormat parameter returns a pRequestedInputFormat pointer and the IsInputFormatSupported method returns a value of S_OK. Otherwise, this method returns one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The format of the input/output format pair is not supported. ppSupportedInputFormat returns a suggested new format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_FORMAT_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The format to be verified is not supported. The value of ppSupportedInputFormat does not change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer that is passed to the method. The value of ppSupportedInputFormat does not change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other HRESULT values</b></dt>
</dl>
</td>
<td width="60%">
These additional error conditions are tracked by the audio engine.

</td>
</tr>
</table>
 




## -remarks



There are differences in the implementation of the <code>IsInputFormatSupported</code> method by the different APOs. For example, with certain implementations, the output can only be of type float when the input format is of type integer.

To initiate format negotiation, the audio service first sets the output of the LFX sAPO to the default float32-based format. The audio service then calls the <code>IAudioProcessingObject::IsInputFormatSupported</code> method of the LFX sAPO, suggests the default format, and monitors the HRESULT response of this method. If the input of the LFX sAPO can support the suggested format, it returns S_OK, together with a reference to the supported format. If the input of the LFX sAPO cannot support the suggested format, it returns S_FALSE together with a reference to a format that is the closest match to the suggested one. If the LFX sAPO cannot support the suggested format and does not have a close match, it returns APOERR_FORMAT_NOT_SUPPORTED. The GFX sAPO works with the output format of the LFX sAPO. So the GFX sAPO is not involved in the format negotiation process.



