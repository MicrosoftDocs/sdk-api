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

# SslGetServerIdentity function


## -description


The <b>SslGetServerIdentity</b> function gets the identity of the server. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Schannel.dll.


## -parameters




### -param ClientHello [in]

The message from the client.


### -param ClientHelloSize [in]

The size of the client message.


### -param ServerIdentity [out]

The pointer inside the message where the server name starts. 


### -param ServerIdentitySize [out]

The length of the server name.


### -param Flags [in]

This parameter is reserved and must be zero.


## -returns



The status of the call to the function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OK</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters <i>ClientHello</i>, <i>ServerIdentity</i>, or <i>ServerIdentitySize</i> is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INCOMPLETE_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
The  <i>ServerIdentitySize</i> parameter is smaller than the <i>ClientHelloSize</i> parameter.

</td>
</tr>
</table>
 



