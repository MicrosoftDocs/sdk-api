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

# CSecureChannelServer::SACAuth


## -description



The <b>SACAuth</b> method establishes a secure authenticated channel between components.




## -parameters




### -param dwProtocolID

<b>DWORD</b> specifying the protocol identifier. This parameter must be set to SAC_PROTOCOL_V1.


### -param dwPass

<b>DWORD</b> containing the number of the current pass.


### -param pbDataIn [in]

Pointer to the first byte of the input authentication data.


### -param dwDataInLen

<b>DWORD</b> specifying the length of the data to which <i>pbDataIn</i> points.


### -param ppbDataOut [out]

Pointer to a pointer to the output authentication data.


### -param pdwDataOutLen

Pointer to a <b>DWORD</b> specifying the length of the data to which <i>ppbDataOut</i> points.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



This method is called one or more times as dictated by the protocol identifier. The structure of the data in <i>pbDataIn</i> and <i>pbDataOut</i> is determined by the values of <i>dwProtocolID</i> and <i>dwPass</i>. The <i>dwPass</i> parameter indicates the number of the communication pass that is under way.

This method is used by the service provider to implement the public <a href="https://msdn.microsoft.com/26cecd09-5f28-47e5-92ec-c2f277be8052">IComponentAuthenticate::SACAuth</a> method. For an example of calling this method, see that method's documentation.




## -see-also




<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>



<a href="https://msdn.microsoft.com/26cecd09-5f28-47e5-92ec-c2f277be8052">IComponentAuthenticate::SACAuth</a>



<a href="https://msdn.microsoft.com/6cb49f6b-e303-4840-9343-9891e75e07a4">Message Authentication</a>
 

 

