---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorGetInfo
title: EapMethodAuthenticatorGetInfo function (eapmethodauthenticatorapis.h)
author: windows-sdk-content
description: Obtains a set of function pointers for an implementation of the loaded EAP authenticator method.EapMethodAuthenticatorGetInfo is a function prototype.
old-location: eaphost\eapmethodauthenticatorgetinfo.htm
tech.root: eaphost
ms.assetid: 83a643bb-5d2e-4227-b82e-e63035860f46
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EapMethodAuthenticatorGetInfo, EapMethodAuthenticatorGetInfo function [EAPHost], eaphost.eapmethodauthenticatorgetinfo, eapmethodauthenticatorapis/EapMethodAuthenticatorGetInfo
ms.topic: function
req.header: eapmethodauthenticatorapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - eapmethodauthenticatorapis.h
api_name:
 - EapMethodAuthenticatorGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapMethodAuthenticatorGetInfo function


## -description


Obtains a set of function pointers for an implementation of the loaded EAP authenticator method.<b>EapMethodAuthenticatorGetInfo</b> is a function prototype. 




## -parameters




### -param pEapType [in]

A pointer to an <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains the vendor ID of the EAPHost authenticator function implementer.


### -param pEapInfo [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa363640(v=VS.85).aspx">EAP_AUTHENTICATOR_METHOD_ROUTINES</a> structure that contains the function pointers to EAP method-specific implementations of the APIs that correspond to specific RPC calls that can be made by EAP peer method functions.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -remarks



Every EAP authenticator method DLL must have public implementations of the following APIs on it:

<ul>
<li>
<a href="https://msdn.microsoft.com/19484962-01fa-4abe-a6b4-c05b8112b0aa">EapMethodAuthenticatorInitialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/13ca6504-63c6-4dd6-a3bf-0f3929bc527f">EapMethodAuthenticatorUpdateInnerMethodParams</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93505c06-fc77-44e6-8ca2-e52ee67ca267">EapMethodAuthenticatorReceivePacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5227ff56-8ac3-4fd7-b6c0-c2d3ef6b906e">EapMethodAuthenticatorSendPacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/531a95c9-b804-4151-b571-163f870672bb">EapMethodAuthenticatorGetAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0cc4df3a-6438-4770-9b13-c9d2a798822c">EapMethodAuthenticatorSetAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/898b5465-a030-4df6-a51f-0725c6332e80">EapMethodAuthenticatorGetResult</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6295277d-3ad8-4c37-a6bf-8f72e8a9b404">EapMethodAuthenticatorEndSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b6f883f-f3ea-48d0-b61c-9056316cd232">EapMethodAuthenticatorShutdown</a>
</li>
</ul>
These APIs are called on an EAP authenticator method when an authenticator (server) EAPHost receives a specific corresponding RPC call from  a peer (client) EAP method.  Note that a complete one-to-one correspondence does not exist between EAP peer methods and EAP authenticator methods; the specific EAP authenticator method API calls should be made based on the requirements of your implementation of the EAP authenticator method API calls.

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>
 

 

