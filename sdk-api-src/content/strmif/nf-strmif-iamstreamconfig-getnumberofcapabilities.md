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

# IAMStreamConfig::GetNumberOfCapabilities


## -description



The <code>GetNumberOfCapabilities</code> method retrieves the number of format capabilities that this pin supports.




## -parameters




### -param piCount [out]

Pointer to a variable that receives the number of format capabilities.


### -param piSize [out]

Pointer to a variable that receives the size of the configuration structure in bytes. See Remarks for more information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The input pin is not connected.

</td>
</tr>
</table>
 




## -remarks



An output pin can support more than one set of format capabilities. This method returns the total number of capabilities that the pin supports; the number is returned in the <i>piCount</i> parameter. To retrieve a particular set of capabilities, call the <a href="https://msdn.microsoft.com/9dd84847-2cae-42f2-a858-7106cd2ac075">IAMStreamConfig::GetStreamCaps</a> method. Format capabilities are indexed from zero, so the value returned in <i>piCount</i> is one more than the upper bound.

Depending on the pin's format type, the <b>GetStreamCaps</b> method returns either a <a href="https://msdn.microsoft.com/c4e68065-79d0-4e2e-abe5-2e5b6a51bd40">VIDEO_STREAM_CONFIG_CAPS</a> structure (for video) or an <a href="https://msdn.microsoft.com/8a923e8e-173e-4258-ba81-7d398bd9c5fe">AUDIO_STREAM_CONFIG_CAPS</a> structure (for audio). The <i>piSize</i> parameter receives the size of the structure, in bytes.

On some compression filters, this method fails if the filter's input pin is not connected.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c171763e-9108-49a0-a4b7-855c6db0a71d">IAMStreamConfig Interface</a>
 

 

