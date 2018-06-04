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

# IOCSPCAConfiguration::put_ProviderProperties


## -description


The <b>ProviderProperties</b> property gets or sets information that provides certificate status responses. The revocation information provider configured in the <a href="https://msdn.microsoft.com/4ea109a9-00ed-46b5-a58c-7dc5bc936102">ProviderCLSID</a> property uses <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs) specified in this property to provide responses.

This property is read/write.


## -parameters


## -remarks



The <b>VARIANT</b> returned in <i>pVal</i> is an <a href="https://msdn.microsoft.com/8c700357-0cb4-4780-9ff1-ac57c46f9183">IOCSPPropertyCollection</a> interface.

To work with revocation-information provider properties:

<ol>
<li>Create an <a href="https://msdn.microsoft.com/8c700357-0cb4-4780-9ff1-ac57c46f9183">IOCSPPropertyCollection</a> object.</li>
<li>Call <a href="https://msdn.microsoft.com/e944af4e-80e4-470e-be04-770cf0f89871">InitializeFromProperties</a> and pass in the <b>VARIANT</b>, <i>pVal</i>, returned by the <b>ProviderProperties</b> property.</li>
<li>Use the <a href="https://msdn.microsoft.com/7273a8ed-cf0e-40d8-8cac-4effbdf41ae8">Methods</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a> of the <a href="https://msdn.microsoft.com/8c700357-0cb4-4780-9ff1-ac57c46f9183">IOCSPPropertyCollection</a> interface.</li>
</ol>
The following table lists the possible <a href="https://msdn.microsoft.com/854848f0-ea89-4c25-a8a5-40f1e4d229be">IOCSPProperty</a> <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> values and their data types for the default revocation-information provider.

<table>
<tr>
<th>Name</th>
<th>Data type</th>
</tr>
<tr>
<td>BaseCrl</td>
<td>Depends on BaseCrlUrl</td>
</tr>
<tr>
<td>BaseCrlUrl </td>
<td>REG_MULTI_SZ</td>
</tr>
<tr>
<td>CrlUrlTimeout</td>
<td>DWORD</td>
</tr>
<tr>
<td>DeltaCrl</td>
<td>Depends on BaseCrlUrl or DeltaCrlUrl</td>
</tr>
<tr>
<td>DeltaCrlUrl</td>
<td>REG_MULTI_SZ</td>
</tr>
<tr>
<td>RefreshTimeOut</td>
<td>DWORD</td>
</tr>
<tr>
<td>RevocationErrorCode</td>
<td>DWORD</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

