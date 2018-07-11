---
UID: NF:eappapis.EapHostPeerGetDataToUnplumbCredentials
title: EapHostPeerGetDataToUnplumbCredentials function
author: windows-sdk-content
description: Returns the Connection Id,User Impersonation Token and Eaphost Process Id used by EAPHost to save the credentials for SSO. This data is needed to unplumb previously plumbed credentials.
old-location: eaphost\eaphostpeergetdatatounplumbcredentials.htm
old-project: eaphost
ms.assetid: E0796AA8-594F-4B21-884D-BD2DD6E2549C
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: EapHostPeerGetDataToUnplumbCredentials, EapHostPeerGetDataToUnplumbCredentials function [EAPHost], eaphost.eaphostpeergetdatatounplumbcredentials, eappapis/EapHostPeerGetDataToUnplumbCredentials
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EapPacket
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerGetDataToUnplumbCredentials
product: Windows
targetos: Windows
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerGetDataToUnplumbCredentials function


## -description


Returns the<b> Connection Id</b>,<b>User Impersonation Token</b> and <b>Eaphost Process Id  </b>used by EAPHost to save the credentials for SSO. This data is needed to unplumb previously plumbed credentials.
<div class="alert"><b>Important</b>   
Unplumbing of credentials (plumbed as part of the SSO experience) on disconnection is no longer performed by EAPHost. Unplumbing of credentials now needs to be performed by the supplicant. </div><div> </div>

## -parameters




### -param pConnectionIdThatLastSavedCreds [out]

The  GUID of the EAP peer session that last plumbed credentials.


### -param phCredentialImpersonationToken [out]

Handle to impersonate the user at the time of plumbing credentials. The user can be impersonated by a call to <b>ImpersonateLoggedOnUser</b>. 



### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


### -param fSaveToCredMan

TBD




#### - phEapHostProcess [out]

A pseudo handle to the EAPHost process. This is the  __int3264 value returned to EAPHost when it called <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>. 



## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>



<a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>
 

 

