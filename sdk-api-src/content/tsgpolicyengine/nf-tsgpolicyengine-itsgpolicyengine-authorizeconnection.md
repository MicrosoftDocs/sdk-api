---
UID: NF:tsgpolicyengine.ITSGPolicyEngine.AuthorizeConnection
title: ITSGPolicyEngine::AuthorizeConnection (tsgpolicyengine.h)
description: Determines whether the specified connection is authorized to connect to Remote Desktop Gateway (RD Gateway).
helpviewer_keywords: ["AuthorizeConnection","AuthorizeConnection method [Remote Desktop Services]","AuthorizeConnection method [Remote Desktop Services]","ITSGPolicyEngine interface","ITSGPolicyEngine interface [Remote Desktop Services]","AuthorizeConnection method","ITSGPolicyEngine.AuthorizeConnection","ITSGPolicyEngine::AuthorizeConnection","termserv.itsgpolicyengine_authorizeconnection","tsgpolicyengine/ITSGPolicyEngine::AuthorizeConnection"]
old-location: termserv\itsgpolicyengine_authorizeconnection.htm
tech.root: TermServ
ms.assetid: 41a61eef-c8fe-4e08-b793-a58553f31646
ms.date: 12/05/2018
ms.keywords: AuthorizeConnection, AuthorizeConnection method [Remote Desktop Services], AuthorizeConnection method [Remote Desktop Services],ITSGPolicyEngine interface, ITSGPolicyEngine interface [Remote Desktop Services],AuthorizeConnection method, ITSGPolicyEngine.AuthorizeConnection, ITSGPolicyEngine::AuthorizeConnection, termserv.itsgpolicyengine_authorizeconnection, tsgpolicyengine/ITSGPolicyEngine::AuthorizeConnection
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSGPolicyEngine::AuthorizeConnection
 - tsgpolicyengine/ITSGPolicyEngine::AuthorizeConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGPolicyEngine.AuthorizeConnection
---

# ITSGPolicyEngine::AuthorizeConnection


## -description

Determines whether the specified connection is authorized to connect to  Remote Desktop Gateway (RD Gateway).

RD Gateway calls this method after a user has been successfully authenticated. The authorization plug-in should then use the <a href="/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeconnectionsink">ITSGAuthorizeConnectionSink</a>  interface to notify RD Gateway about the result of authorization.

## -parameters

### -param mainSessionId [in]

A unique identifier assigned to the connection request by RD Gateway.

### -param username [in]

The user name.

### -param authType [in]

A value of the <a href="/windows/win32/api/tsgpolicyengine/ne-tsgpolicyengine-aaauthschemes">AAAuthSchemes</a> enumeration type that specifies the type of authentication used to connect to RD Gateway.

### -param clientMachineIP [in]

The IP address of the user's computer.

### -param clientMachineName [in]

The name of the user's computer.

### -param sohData [in]

A pointer to a <b>BYTE</b> that contains the statement of health (SoH) provided by the user's computer. If the authorization plug-in does not require a statement of health, this parameter is <b>NULL</b>. For more information, see the <a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-isquarantineenabled">IsQuarantineEnabled</a> method.

### -param numSOHBytes [in]

The number of bytes referenced by the <i>sohData</i> parameter.

### -param cookieData [in]

A pointer to a <b>BYTE</b> that contains the cookie provided by the user. If the <b>authType</b> parameter is not set to <b>AA_AUTH_COOKIE</b>, this parameter is <b>NULL</b>.

### -param numCookieBytes [in]

The number of bytes referenced by the <i>cookieData</i> parameter.

### -param userToken [in]

A pointer to a <b>HANDLE</b> that specifies the user token of the user. If the user is not running Windows, this parameter is <b>NULL</b>.

### -param pSink [in]

A pointer to an <a href="/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeconnectionsink">ITSGAuthorizeConnectionSink</a> interface that the authorization plug-in must use to notify RD Gateway about the result of authorization.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method returns <b>S_OK</b>, RD Gateway waits for the authorization 
    plug-in to call a method of the 
    <a href="/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeconnectionsink">ITSGAuthorizeConnectionSink</a> interface. If 
    any other value is returned, RD Gateway immediately denies the  authorization request.

If authorization requires more than 1 second, we recommend starting a separate thread to perform 
    authorization.

For a sample that uses the <b>AuthorizeConnection</b> method, see the [Remote Desktop Gateway Pluggable Authentication and Authorization](https://github.com/microsoftarchive/msdn-code-gallery-community-m-r/tree/master/Remote%20Desktop%20Gateway%20Pluggable%20Authentication%20and%20Authorization%20Sample) sample.

## -see-also

<a href="/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeconnectionsink">ITSGAuthorizeConnectionSink</a>



<a href="/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgpolicyengine">ITSGPolicyEngine</a>



<a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-isquarantineenabled">IsQuarantineEnabled</a>