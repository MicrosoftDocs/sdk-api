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

# IMFASFStreamConfig::GetPayloadExtension


## -description



Retrieves information about an existing payload extension.




## -parameters




### -param wPayloadExtensionNumber [in]

The payload extension index. Valid indexes range from 0, to one less than the number of extensions obtained by calling <a href="https://msdn.microsoft.com/3b1cb5a9-e39c-4f16-abc1-45ab516a4b80">IMFASFStreamConfig::GetPayloadExtensionCount</a>.


### -param pguidExtensionSystemID [out]

Receives a GUID that identifies the payload extension. For a list of predefined payload extensions, see <a href="https://msdn.microsoft.com/db973b41-1e5c-4bc8-921d-5e9312eb21cb">ASF Payload Extension GUIDs</a>. Applications can also define custom payload extensions.


### -param pcbExtensionDataSize [out]

Receives the number of bytes added to each sample for the extension.


### -param pbExtensionSystemInfo [out]

Pointer to a buffer that receives information about this extension system. This information is the same for all samples and is stored in the content header (not in each sample). This parameter can be <b>NULL</b>. To find the required size of the buffer, set this parameter to <b>NULL</b>; the size is returned in <i>pcbExtensionSystemInfo</i>.


### -param pcbExtensionSystemInfo [in, out]

On input, specifies the size of the buffer pointed to by <i>pbExtensionSystemInfo</i>. On output, receives the required size of the <i>pbExtensionSystemInfo</i> buffer in bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified in <i>pbExtensionSystemInfo</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>wPayloadExtensionNumber</i> parameter is out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>



<a href="https://msdn.microsoft.com/55dd4125-ce44-4eed-b1a8-74819c452bd4">IMFASFStreamConfig::AddPayloadExtension</a>



<a href="https://msdn.microsoft.com/3b1cb5a9-e39c-4f16-abc1-45ab516a4b80">IMFASFStreamConfig::GetPayloadExtensionCount</a>
 

 

