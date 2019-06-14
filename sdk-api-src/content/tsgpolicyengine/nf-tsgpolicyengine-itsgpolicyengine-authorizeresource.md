---
UID: NF:tsgpolicyengine.ITSGPolicyEngine.AuthorizeResource
title: ITSGPolicyEngine::AuthorizeResource (tsgpolicyengine.h)
author: windows-sdk-content
description: Determines which resources the specified connection is authorized to connect to.
old-location: termserv\itsgpolicyengine_authorizeresource.htm
tech.root: TermServ
ms.assetid: 77950541-c94a-4035-a2d8-a6014eb387e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AuthorizeResource, AuthorizeResource method [Remote Desktop Services], AuthorizeResource method [Remote Desktop Services],ITSGPolicyEngine interface, ITSGPolicyEngine interface [Remote Desktop Services],AuthorizeResource method, ITSGPolicyEngine.AuthorizeResource, ITSGPolicyEngine::AuthorizeResource, termserv.itsgpolicyengine_authorizeresource, tsgpolicyengine/ITSGPolicyEngine::AuthorizeResource
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGPolicyEngine.AuthorizeResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGPolicyEngine::AuthorizeResource


## -description


Determines which resources the specified connection is authorized to connect to.

Remote Desktop Gateway (RD Gateway) calls this method after a user has been successfully authenticated. The authorization plug-in should then use the <a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeconnectionsink">ITSGAuthorizeConnectionSink</a>  interface to notify RD Gateway about the result of authorization.


## -parameters




### -param mainSessionId [in]

A unique identifier assigned to the connection request by RD Gateway.


### -param subSessionId [in]

A unique identifier assigned to the subsession by RD Gateway. A subsession is a session launched from another session.


### -param username [in]

The user name.


### -param resourceNames [in]

A list of resources to authorize.


### -param numResources [in]

The number of resources referenced by the <i>resourceNames</i> parameter.


### -param alternateResourceNames [in]

A pointer to a <b>BSTR</b> that contains a list of alternate resource names. This parameter is only valid when RD Connection Broker is in use.


### -param numAlternateResourceName [in]

The number of alternate resource names referenced by the <i>alternateResourceNames</i> parameter.


### -param portNumber [in]

The port number specified by the user.


### -param operation [in]

The operation that the user is attempting on the resource. This parameter is always set to "RDP".


### -param cookie [in]

A pointer to a <b>BYTE</b> that contains the cookie provided by the user. If the user did not authenticate by using a cookie, this parameter is <b>NULL</b>.


### -param numBytesInCookie [in]

The number of bytes referenced by the <i>cookie</i> parameter.


### -param pSink [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeresourcesink">ITSGAuthorizeResourceSink</a> interface that the authorization plug-in must use to notify RD Gateway about the result of authorization.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method returns <b>S_OK</b>, RD Gateway waits for the authorization 
    plug-in to call a method of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeresourcesink">ITSGAuthorizeResourceSink</a> interface. If any 
    other value is returned, RD Gateway immediately denies the  authorization request.

If authorization requires more than 1 second, we recommend starting a separate thread to perform 
    authorization.


#### Examples

For an example that uses the 
     <b>AuthorizeResource</b> method, see 
     <a href="https://Code.MSDN.Microsoft.Com/Remote-Desktop-Gateway-517d6273">Remote Desktop Gateway Pluggable Authentication and Authorization Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgpolicyengine">ITSGPolicyEngine</a>
 

 

