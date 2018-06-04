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

# ICredentialProviderCredential::GetSerialization


## -description


Called in response to an attempt to submit this credential to the underlying authentication engine.


## -parameters




### -param pcpgsr [out]

Type: <b><a href="https://msdn.microsoft.com/73615129-62f2-4bc9-acf6-058a6641f4e2">CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE</a>*</b>

Indicates the success or failure of the attempt to serialize credentials.


### -param pcpcs [out]

Type: <b><a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A pointer to the credential. Depending on the result, there may be no valid credential.


### -param ppszOptionalStatusText [out]

Type: <b>LPWSTR*</b>

A pointer to a Unicode string value that will be displayed by the Logon UI after serialization. May be <b>NULL</b>.


### -param pcpsiOptionalStatusIcon [out]

Type: <b><a href="https://msdn.microsoft.com/2aa5b5dc-4756-4eff-a7d8-97c8a1dce41b">CREDENTIAL_PROVIDER_STATUS_ICON</a>*</b>

A pointer to an icon that will be displayed by the credential after the call to <b>GetSerialization</b> returns. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required.

The <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> indicates what the appropriate response would be when the user attempts to submit credentials. The following table indicates how to respond based on the usage scenario.

<table>
<tr>
<td><b>CPUS_CHANGE_PASSWORD</b></td>
<td>No credential serialization occurs in this scenario. In this scenario the credential provider should update the user's private information and return <b>CPGSR_NO_CREDENTIAL_FINISHED</b> as <i>pcpgsr.</i></td>
</tr>
<tr>
<td><b>CPUS_CREDUI</b></td>
<td>The credential information should be serialized and delivered to the calling application.</td>
</tr>
<tr>
<td><b>CPUS_LOGON</b>, <b>CPUS_UNLOCK_WORKSTATION</b></td>
<td>The credential information should be packed into a binary stream and transmitted to <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> and eventually LSA.</td>
</tr>
</table>
 

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>


