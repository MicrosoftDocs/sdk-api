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

# ITSGPolicyEngine::AuthorizeConnection


## -description


Determines whether the specified connection is authorized to connect to  Remote Desktop Gateway (RD Gateway).

RD Gateway calls this method after a user has been successfully authenticated. The authorization plug-in should then use the <a href="https://msdn.microsoft.com/4aa6ec0d-6525-46e1-ba0b-29d80c5ee0f1">ITSGAuthorizeConnectionSink</a>  interface to notify RD Gateway about the result of authorization.


## -parameters




### -param mainSessionId [in]

A unique identifier assigned to the connection request by RD Gateway.


### -param username [in]

The user name.


### -param authType [in]

A value of the <a href="https://msdn.microsoft.com/ff80f8ac-8378-4087-aa95-a081d2dd710a">AAAuthSchemes</a> enumeration type that specifies the type of authentication used to connect to RD Gateway. 


### -param clientMachineIP [in]

The IP address of the user's computer.


### -param clientMachineName [in]

The name of the user's computer.


### -param sohData [in]

A pointer to a <b>BYTE</b> that contains the statement of health (SoH) provided by the user's computer. If the authorization plug-in does not require a statement of health, this parameter is <b>NULL</b>. For more information, see the <a href="https://msdn.microsoft.com/e63b99ba-068f-4842-b00a-9bfc5f8dac73">IsQuarantineEnabled</a> method.


### -param numSOHBytes [in]

The number of bytes referenced by the <i>sohData</i> parameter.


### -param cookieData [in]

A pointer to a <b>BYTE</b> that contains the cookie provided by the user. If the <b>authType</b> parameter is not set to <b>AA_AUTH_COOKIE</b>, this parameter is <b>NULL</b>.


### -param numCookieBytes [in]

The number of bytes referenced by the <i>cookieData</i> parameter.


### -param userToken [in]

A pointer to a <b>HANDLE</b> that specifies the user token of the user. If the user is not running Windows, this parameter is <b>NULL</b>.


### -param pSink [in]

A pointer to an <a href="https://msdn.microsoft.com/4aa6ec0d-6525-46e1-ba0b-29d80c5ee0f1">ITSGAuthorizeConnectionSink</a> interface that the authorization plug-in must use to notify RD Gateway about the result of authorization.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method returns <b>S_OK</b>, RD Gateway waits for the authorization 
    plug-in to call a method of the 
    <a href="https://msdn.microsoft.com/4aa6ec0d-6525-46e1-ba0b-29d80c5ee0f1">ITSGAuthorizeConnectionSink</a> interface. If 
    any other value is returned, RD Gateway immediately denies the  authorization request.

If authorization requires more than 1 second, we recommend starting a separate thread to perform 
    authorization.


#### Examples

For an example that uses the 
     <b>AuthorizeConnection</b> method, see 
     <a href="https://Code.MSDN.Microsoft.Com/Remote-Desktop-Gateway-517d6273">Remote Desktop Gateway Pluggable Authentication and Authorization Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4aa6ec0d-6525-46e1-ba0b-29d80c5ee0f1">ITSGAuthorizeConnectionSink</a>



<a href="https://msdn.microsoft.com/1972032f-48ac-4a15-98ce-9349fa158a07">ITSGPolicyEngine</a>



<a href="https://msdn.microsoft.com/e63b99ba-068f-4842-b00a-9bfc5f8dac73">IsQuarantineEnabled</a>
 

 

