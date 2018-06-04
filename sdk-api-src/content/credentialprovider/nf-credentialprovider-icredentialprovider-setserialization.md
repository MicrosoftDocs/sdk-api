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

# ICredentialProvider::SetSerialization


## -description


Sets the serialization characteristics of the credential provider.


## -parameters




### -param pcpcs [in]

Type: <b>const <a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure that stores the serialization characteristics of the credential provider.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required. It accepts a credential and determines if <i>pcpcs</i> was a partial or a full credential. If it is a partial credential, it is either incomplete or was passed for the purpose of displaying some information to the user. If it is a full credential, it should be serialized and submitted. Use the members of the <a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> and the flags passed in <a href="https://msdn.microsoft.com/62577b41-e115-45df-9f9b-c5c282365a3e">SetUsageScenario</a> to determine how to handle the input. The responsibility is on the credential provider to verify the integrity of the input. The Credential UI and Logon UI do not perform any checks on the structure before passing it to the credential provider.

<b>SetSerialization</b> is always called after <a href="https://msdn.microsoft.com/62577b41-e115-45df-9f9b-c5c282365a3e">SetUsageScenario</a>. The Logon UI also calls <b>SetSerialization</b> when a filter returns a credential through <a href="https://msdn.microsoft.com/d0730f67-e4f1-42b2-823a-75b08a5c952e">UpdateRemoteCredential</a>. It does not use this method when re-enumerating tiles because of a call to <a href="https://msdn.microsoft.com/bff835ed-01b9-4620-a97c-c64a2445e02a">CredentialsChanged</a>. The Credential UI calls <b>SetSerialization</b> when an input credential has been suppled by an application.

The Credential UI enforces the following rules based on the <i>dwFlags</i> for this content provider instance defined when <a href="https://msdn.microsoft.com/62577b41-e115-45df-9f9b-c5c282365a3e">SetUsageScenario</a> was called.

<ul>
<li>If the flags include <b>CREDUIWIN_IN_CRED_ONLY</b>, all credential providers returning <b>S_OK</b> are enabled.</li>
<li>If the flags include <b>CREDUIWIN_AUTHPACKAGE_ONLY</b>, all credential providers returning a success status are enabled.</li>
<li>If neither of those flags are included, then the Credential UI follows the same logic as the Logon UI and all credential providers that implement the <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a><b>CPUS_REDUI</b> will be enabled regardless of the returned status value.</li>
</ul>
Credential providers that implement a <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> of <b>CPUS_LOGON</b> and return a failure from this method will still be enabled.



