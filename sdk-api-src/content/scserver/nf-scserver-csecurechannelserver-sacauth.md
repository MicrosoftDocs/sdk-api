---
UID: NF:scserver.CSecureChannelServer.SACAuth
title: CSecureChannelServer::SACAuth
author: windows-sdk-content
description: The SACAuth method establishes a secure authenticated channel between components.
old-location: wmdm\csecurechannelserver_sacauth.htm
tech.root: WMDM
ms.assetid: e32aac59-4b7f-4c0e-a200-0dec50d89cb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CSecureChannelServer interface [windows Media Device Manager],SACAuth method, CSecureChannelServer.SACAuth, CSecureChannelServer::SACAuth, CSecureChannelServerSACAuth, SACAuth, SACAuth method [windows Media Device Manager], SACAuth method [windows Media Device Manager],CSecureChannelServer interface, scserver/CSecureChannelServer::SACAuth, wmdm.csecurechannelserver_sacauth
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: scserver.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelServer.SACAuth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.

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
 

 

