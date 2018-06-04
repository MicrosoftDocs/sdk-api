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

# IMFNetSchemeHandlerConfig::GetSupportedProtocolType


## -description



Retrieves a supported protocol by index




## -parameters




### -param nProtocolIndex [in]

Zero-based index of the protocol to retrieve. To get the number of supported protocols, call <a href="https://msdn.microsoft.com/a0cbb01c-c86c-4186-81ca-6055aab5d361">IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols</a>.


### -param pnProtocolType [out]

Receives a member of the <a href="https://msdn.microsoft.com/dd628b9e-3c52-4c14-aa0f-5e0b811d3f57">MFNETSOURCE_PROTOCOL_TYPE</a> enumeration.


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
The value passed in the <i>nProtocolIndex</i> parameter was greater than the total number of supported protocols, returned by <a href="https://msdn.microsoft.com/a0cbb01c-c86c-4186-81ca-6055aab5d361">GetNumberOfSupportedProtocols</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/91bdcdbd-d621-42e3-8e0f-f8eeab489d35">IMFNetSchemeHandlerConfig</a>
 

 

