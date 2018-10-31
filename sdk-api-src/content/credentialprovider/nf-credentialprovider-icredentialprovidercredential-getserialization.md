---
UID: NF:credentialprovider.ICredentialProviderCredential.GetSerialization
title: ICredentialProviderCredential::GetSerialization
author: windows-sdk-content
description: Called in response to an attempt to submit this credential to the underlying authentication engine.
old-location: shell\ICredentialProviderCredential_GetSerialization.htm
tech.root: shell
ms.assetid: c5f7ba25-c38a-431a-b4ad-0e2409f763a3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetSerialization, GetSerialization method [Windows Shell], GetSerialization method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetSerialization method, ICredentialProviderCredential.GetSerialization, ICredentialProviderCredential::GetSerialization, credentialprovider/ICredentialProviderCredential::GetSerialization, shell.ICredentialProviderCredential_GetSerialization, shell_ICredentialProviderCredential_GetSerialization
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProviderCredential.GetSerialization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<td>The credential information should be packed into a binary stream and transmitted to <a href="https://msdn.microsoft.com/232d1dcc-5388-480c-8d27-caf8ded4575d">Winlogon</a> and eventually LSA.</td>
</tr>
</table>
 

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>


