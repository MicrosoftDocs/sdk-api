---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_USAGE_SCENARIO
title: CREDENTIAL_PROVIDER_USAGE_SCENARIO (credentialprovider.h)
description: Declares the scenarios in which a credential provider is supported. A credential provider usage scenario (CPUS) enables the credential provider to provide distinct enumeration behavior and UI field setup across scenarios.
helpviewer_keywords: ["CPUS_CHANGE_PASSWORD","CPUS_CREDUI","CPUS_INVALID","CPUS_LOGON","CPUS_PLAP","CPUS_UNLOCK_WORKSTATION","CREDENTIAL_PROVIDER_USAGE_SCENARIO","CREDENTIAL_PROVIDER_USAGE_SCENARIO enumeration [Windows Shell]","credentialprovider/CPUS_CHANGE_PASSWORD","credentialprovider/CPUS_CREDUI","credentialprovider/CPUS_INVALID","credentialprovider/CPUS_LOGON","credentialprovider/CPUS_PLAP","credentialprovider/CPUS_UNLOCK_WORKSTATION","credentialprovider/CREDENTIAL_PROVIDER_USAGE_SCENARIO","shell.CREDENTIAL_PROVIDER_USAGE_SCENARIO","shell_CREDENTIAL_PROVIDER_USAGE_SCENARIO"]
old-location: shell\CREDENTIAL_PROVIDER_USAGE_SCENARIO.htm
tech.root: shell
ms.assetid: 86025d1d-b13d-4f61-824a-fd471e449567
ms.date: 12/05/2018
ms.keywords: CPUS_CHANGE_PASSWORD, CPUS_CREDUI, CPUS_INVALID, CPUS_LOGON, CPUS_PLAP, CPUS_UNLOCK_WORKSTATION, CREDENTIAL_PROVIDER_USAGE_SCENARIO, CREDENTIAL_PROVIDER_USAGE_SCENARIO enumeration [Windows Shell], credentialprovider/CPUS_CHANGE_PASSWORD, credentialprovider/CPUS_CREDUI, credentialprovider/CPUS_INVALID, credentialprovider/CPUS_LOGON, credentialprovider/CPUS_PLAP, credentialprovider/CPUS_UNLOCK_WORKSTATION, credentialprovider/CREDENTIAL_PROVIDER_USAGE_SCENARIO, shell.CREDENTIAL_PROVIDER_USAGE_SCENARIO, shell_CREDENTIAL_PROVIDER_USAGE_SCENARIO
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIAL_PROVIDER_USAGE_SCENARIO
 - credentialprovider/_CREDENTIAL_PROVIDER_USAGE_SCENARIO
 - CREDENTIAL_PROVIDER_USAGE_SCENARIO
 - credentialprovider/CREDENTIAL_PROVIDER_USAGE_SCENARIO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credentialprovider.h
api_name:
 - CREDENTIAL_PROVIDER_USAGE_SCENARIO
---

# CREDENTIAL_PROVIDER_USAGE_SCENARIO enumeration


## -description

Declares the scenarios in which a credential provider is supported. A credential provider usage scenario (CPUS) enables the credential provider to provide distinct enumeration behavior and UI field setup across scenarios. When an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider">ICredentialProvider</a> is initialized, it calls <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setusagescenario">ICredentialProvider::SetUsageScenario</a> to set what usage scenario is supported. That scenario is maintained for the entire lifetime of the credential provider.

## -enum-fields

### -field CPUS_INVALID:0

No usage scenario has been set for the credential provider. The scenario is not passed to <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setusagescenario">ICredentialProvider::SetUsageScenario</a>. If a credential provider stores its current usage scenario as a class member, this provides an initialization value before the first call to <b>ICredentialProvider::SetUsageScenario</b>.

### -field CPUS_LOGON

Workstation logon or unlock. See the remarks for more details. Credential providers that implement this scenario should be prepared to serialize credentials to the local authority for authentication.

### -field CPUS_UNLOCK_WORKSTATION

Workstation unlock. Credential providers that implement this scenario should be prepared to serialize credentials to the local authority for authentication. These credential providers also need to enumerate the currently logged-in user as the default tile.

### -field CPUS_CHANGE_PASSWORD

Password change. This enables a credential provider to enumerate tiles in response to a user's request to change the password. Do not implement this scenario if you do not require some secret information from the user such as a password or PIN. These credential providers also need to enumerate the currently logged-in user as the default tile.

### -field CPUS_CREDUI

Credential UI. This scenario enables you to use credentials serialized by the credential provider to be used as authentication on remote machines. This is also the scenario used for over-the-shoulder prompting in User Access Control. This scenario uses a different instance of the credential provider than the one used for <b>CPUS_LOGON</b>, <b>CPUS_UNLOCK_WORKSTATION</b>, and <b>CPUS_CHANGE_PASSWORD</b>, so the state of the credential provider cannot be maintained across the different scenarios.

### -field CPUS_PLAP

Pre-Logon-Access Provider. Credential providers responding to this usage scenario must register under:  

                

<b>HKLM</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows</b>&#92;<b>CurrentVersion</b>&#92;<b>Authentication</b>&#92;<b>PLAP Providers</b>

## -remarks

Starting in Windows 10, the <b>CPUS_LOGON</b> and <b>CPUS_UNLOCK_WORKSTATION</b> user scenarios have been combined. This enables the system to support multiple users logging into a machine without creating and switching sessions unnecessarily. Any user on the machine can log into it once it has been locked without needing to back out of a current session and create a new one. Because of this, <b>CPUS_LOGON</b> can be used both for logging onto a system or when a workstation is unlocked. However, <b>CPUS_LOGON</b> cannot be used in all cases. Because of policy restrictions imposed by various systems, sometimes it is necessary for the user scenario to be <b>CPUS_UNLOCK_WORKSTATION</b>. Your credential provider should be robust enough to create the appropriate credential structure based on the scenario given to it. Windows will request the appropriate user scenario based on the situation. Some of the factors that impact whether or not a <b>CPUS_UNLOCK_WORKSTATION</b> scenario must be used include the following. Note that this is just a subset of possibilities.

<ul>
<li>The operating system of the device.</li>
<li>Whether this is a console or remote session.</li>
<li>Group policies such as hiding entry points for fast user switching, or interactive logon that does not display the user's last name.</li>
</ul>
Credential providers that need to enumerate the currently user logged into the system as the default tile can keep track of the current user or leverage APIs such as <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> to obtain that information.

## -see-also

<a href="/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>
