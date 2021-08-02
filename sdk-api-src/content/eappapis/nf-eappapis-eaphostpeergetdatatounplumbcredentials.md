---
UID: NF:eappapis.EapHostPeerGetDataToUnplumbCredentials
title: EapHostPeerGetDataToUnplumbCredentials function (eappapis.h)
description: Returns the Connection Id,User Impersonation Token and Eaphost Process Id used by EAPHost to save the credentials for SSO. This data is needed to unplumb previously plumbed credentials.
helpviewer_keywords: ["EapHostPeerGetDataToUnplumbCredentials","EapHostPeerGetDataToUnplumbCredentials function [EAPHost]","eaphost.eaphostpeergetdatatounplumbcredentials","eappapis/EapHostPeerGetDataToUnplumbCredentials"]
old-location: eaphost\eaphostpeergetdatatounplumbcredentials.htm
tech.root: eaphost
ms.assetid: E0796AA8-594F-4B21-884D-BD2DD6E2549C
ms.date: 12/05/2018
ms.keywords: EapHostPeerGetDataToUnplumbCredentials, EapHostPeerGetDataToUnplumbCredentials function [EAPHost], eaphost.eaphostpeergetdatatounplumbcredentials, eappapis/EapHostPeerGetDataToUnplumbCredentials
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerGetDataToUnplumbCredentials
 - eappapis/EapHostPeerGetDataToUnplumbCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerGetDataToUnplumbCredentials
---

# EapHostPeerGetDataToUnplumbCredentials function


## -description

Returns the<b> Connection Id</b>,<b>User Impersonation Token</b> and <b>Eaphost Process Id  </b> used by EAPHost to save the credentials for SSO. This data is needed to unplumb previously plumbed credentials.
<div class="alert"><b>Important</b>   
Unplumbing of credentials (plumbed as part of the SSO experience) on disconnection is no longer performed by EAPHost. Unplumbing of credentials now needs to be performed by the supplicant. </div><div> </div>

## -parameters

### -param pConnectionIdThatLastSavedCreds [out]

The  GUID of the EAP peer session that last plumbed credentials.

### -param phCredentialImpersonationToken [out]

Handle to impersonate the user at the time of plumbing credentials. The user can be impersonated by a call to <b>ImpersonateLoggedOnUser</b>.

### -param sessionHandle [out]

A pseudo handle to the EAPHost process. This is the  __int3264 value returned to EAPHost when it called <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>.

### -param ppEapError [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param fSaveToCredMan [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>