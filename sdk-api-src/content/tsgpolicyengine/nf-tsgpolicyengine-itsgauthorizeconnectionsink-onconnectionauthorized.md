---
UID: NF:tsgpolicyengine.ITSGAuthorizeConnectionSink.OnConnectionAuthorized
title: ITSGAuthorizeConnectionSink::OnConnectionAuthorized (tsgpolicyengine.h)
description: Notifies Remote Desktop Gateway (RD Gateway) about the result of an attempt to authorize a connection.
old-location: termserv\itsgauthorizeconnectionsink_onconnectionauthorized.htm
tech.root: TermServ
ms.assetid: 1151aa89-944b-4497-8a8c-c6d67fbd4051
ms.date: 12/05/2018
ms.keywords: ITSGAuthorizeConnectionSink interface [Remote Desktop Services],OnConnectionAuthorized method, ITSGAuthorizeConnectionSink.OnConnectionAuthorized, ITSGAuthorizeConnectionSink::OnConnectionAuthorized, OnConnectionAuthorized, OnConnectionAuthorized method [Remote Desktop Services], OnConnectionAuthorized method [Remote Desktop Services],ITSGAuthorizeConnectionSink interface, SESSION_TIMEOUT_ACTION_DISCONNECT, SESSION_TIMEOUT_ACTION_SILENT_REAUTH, termserv.itsgauthorizeconnectionsink_onconnectionauthorized, tsgpolicyengine/ITSGAuthorizeConnectionSink::OnConnectionAuthorized
f1_keywords:
- tsgpolicyengine/ITSGAuthorizeConnectionSink.OnConnectionAuthorized
dev_langs:
- c++
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
- ITSGAuthorizeConnectionSink.OnConnectionAuthorized
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGAuthorizeConnectionSink::OnConnectionAuthorized


## -description


Notifies Remote Desktop Gateway (RD Gateway) about the result of an  attempt to authorize a connection.


## -parameters




### -param hrIn [in]

The result of the authorization attempt. Specify <b>S_OK</b> to indicate that the attempt succeeded. Specify any other value to indicate that the attempt failed.


### -param mainSessionId [in]

A unique identifier assigned to the connection request by RD Gateway.


### -param cbSoHResponse [in]

The number of bytes referenced by the  <i>pbSoHResponse</i> parameter.


### -param pbSoHResponse [in]

A pointer to a <b>BYTE</b> that specifies the response to the request for a statement of health (SoH). If the <i>hrIn</i> parameter is not <b>S_OK</b>, this parameter is ignored.


### -param idleTimeout [in]

The number of minutes that the connection can remain idle before being disconnected. If the <i>hrIn</i> parameter is not <b>S_OK</b>, this parameter is ignored.


### -param sessionTimeout [in]

 The maximum number of minutes allotted to the session. If the <i>hrIn</i> parameter is not <b>S_OK</b>, this parameter is ignored.


### -param sessionTimeoutAction [in]

The action to be taken when the session times out. If the <i>hrIn</i> parameter is not <b>S_OK</b>, this parameter is ignored. This parameter can be one of the following values.



#### SESSION_TIMEOUT_ACTION_DISCONNECT

Disconnect the session.



#### SESSION_TIMEOUT_ACTION_SILENT_REAUTH

Silently reauthenticate and reauthorize the session.


### -param trustClass [in]

This parameter is reserved. Always set it to  <b>AA_TRUSTEDUSER_TRUSTEDCLIENT</b>. If the <i>hrIn</i> parameter is not <b>S_OK</b>, this parameter is ignored.


### -param policyAttributes [in]

An array of Boolean values  that specify the redirection settings associated with the connection. Each element of the array corresponds to a value of the <a href="https://docs.microsoft.com/windows/win32/api/tsgpolicyengine/ne-tsgpolicyengine-policyattributetype">PolicyAttributeType</a> enumeration. If the <i>hrIn</i> parameter is not <b>S_OK</b>, this parameter is ignored.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can call this method from your implementation of 
    <a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-authorizeconnection">AuthorizeConnection</a>. If 
    authentication requires more than 1 second, we recommend launching a separate thread to perform 
    authentication.


#### Examples

For an example that uses the 
     <b>OnConnectionAuthorized</b> method, see 
     <a href="https://Code.MSDN.Microsoft.Com/Remote-Desktop-Gateway-517d6273">Remote Desktop Gateway Pluggable Authentication and Authorization Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeconnectionsink">ITSGAuthorizeConnectionSink</a>
 

 

