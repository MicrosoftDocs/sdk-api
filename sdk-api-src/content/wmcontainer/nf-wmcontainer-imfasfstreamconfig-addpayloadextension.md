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

# IMFASFStreamConfig::AddPayloadExtension


## -description



Configures a payload extension for the stream.




## -parameters




### -param guidExtensionSystemID [in]

Pointer to a GUID that identifies the payload extension. For a list of predefined payload extensions, see <a href="https://msdn.microsoft.com/db973b41-1e5c-4bc8-921d-5e9312eb21cb">ASF Payload Extension GUIDs</a>. Applications can also define custom payload extensions.


### -param cbExtensionDataSize [in]

Number of bytes added to each sample for the extension.


### -param pbExtensionSystemInfo [in]

A pointer to a buffer that contains information about this extension system. This information is the same for all samples and is stored in the content header (not with each sample). This parameter can be <b>NULL</b> if <i>cbExtensionSystemInfo</i> is 0.


### -param cbExtensionSystemInfo [in]

Amount of data, in bytes, that describes this extension system. If this value is 0, then <i>pbExtensionSystemInfo</i> can be <b>NULL</b>.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>



<a href="https://msdn.microsoft.com/5b3b831c-2218-4a76-8359-7f39cab53a57">IMFASFStreamConfig::GetPayloadExtension</a>
 

 

