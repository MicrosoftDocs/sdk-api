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

# IAudioProcessingObject::IsOutputFormatSupported


## -description


The <code>IsOutputFormatSupported</code> method is used to verify that a specific output format is supported.


## -parameters




### -param pOppositeFormat [in, optional]

A pointer to an IAudioMediaType interface. This parameter indicates the output format. This parameter must be set to <b>NULL</b> to indicate that the output format can be any type.


### -param pRequestedOutputFormat [in, optional]

A pointer to an <b>IAudioMediaType</b> interface. This parameter indicates the output format that is to be verified.


### -param ppSupportedOutputFormat [out, optional]

This parameter indicates the supported output format that is closest to the format to be verified.


## -returns



If the call completes successfully, the ppSupportedOutputFormat parameter returns a pRequestedOutputFormat pointer and the IsOutputFormatSupported method returns a value of S_OK. Otherwise, this method returns one of the following error codes:

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
The format of Input/output format pair is not supported. The ppSupportedOutPutFormat parameter returns a suggested new format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_FORMAT_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The format is not supported. The value of ppSupportedOutputFormat does not change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
An invalid pointer was passed to the function. The value of ppSupportedOutputFormat does not change.

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



There are differences in the implementation of the <code>IsOutputFormatSupported</code> method by the different APOs. For example, with certain implementations, the output can only be of type float when the input format is of type integer. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536496">IAudioMediaType</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536501">IAudioProcessingObject</a>
 

 

