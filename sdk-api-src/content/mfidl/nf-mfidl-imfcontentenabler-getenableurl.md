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

# IMFContentEnabler::GetEnableURL


## -description



Retrieves a URL for performing a manual content enabling action.




## -parameters




### -param ppwszURL [out]

Receives a pointer to a buffer that contains the URL. The caller must release the memory for the buffer by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param pcchURL [out]

Receives the number of characters returned in <i>ppwszURL</i>, including the terminating NULL character.


### -param pTrustStatus [in, out]

Receives a member of the <a href="https://msdn.microsoft.com/fd008a23-71f7-4718-a51a-ee88453b6fdd">MF_URL_TRUST_STATUS</a> enumeration indicating whether the URL is trusted.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No URL is available.

</td>
</tr>
</table>
 




## -remarks



If the enabling action can be performed by navigating to a URL, this method returns the URL. If no such URL exists, the method returns a failure code.

The purpose of the URL depends on the content enabler type, which is obtained by calling <a href="https://msdn.microsoft.com/9fe597d8-788c-48c4-a21a-0b91a890710f">IMFContentEnabler::GetEnableType</a>.

<table>
<tr>
<th>Enable type</th>
<th>Purpose of URL</th>
</tr>
<tr>
<td>Individualization</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>License acquisition</td>
<td>URL to obtain the license. Call <a href="https://msdn.microsoft.com/d1859037-7a33-4943-8ca9-6782fc8b0b92">IMFContentEnabler::GetEnableData</a> and submit the data to the URL as an HTTP POST request. To receive notification when the license is acquired, call <a href="https://msdn.microsoft.com/78fc4a17-f58c-4654-b37e-6b988848ff0d">IMFContentEnabler::MonitorEnable</a>.</td>
</tr>
<tr>
<td>Revocation</td>
<td>URL to a webpage where the user can download and install an updated component.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/85d98f49-8af2-42ce-9b36-a025aee93f73">How to Play Protected Media Files</a>



<a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a>
 

 

