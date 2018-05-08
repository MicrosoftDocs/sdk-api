---
UID: NF:credentialprovider.ICredentialProvider.GetCredentialCount
title: ICredentialProvider::GetCredentialCount
author: windows-driver-content
description: Gets the number of available credentials under this credential provider.
old-location: shell\ICredentialProvider_GetCredentialCount.htm
old-project: shell
ms.assetid: 7d940d46-d4c2-4ab5-8559-416d78d3579e
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetCredentialCount, GetCredentialCount method [Windows Shell], GetCredentialCount method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetCredentialCount method, ICredentialProvider.GetCredentialCount, ICredentialProvider::GetCredentialCount, credentialprovider/ICredentialProvider::GetCredentialCount, shell.ICredentialProvider_GetCredentialCount, shell_ICredentialProvider_GetCredentialCount
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
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Credentialprovider.h
api_name:
-	ICredentialProvider.GetCredentialCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProvider::GetCredentialCount


## -description


Gets the number of available credentials under this credential provider.


## -parameters




### -param pdwCount [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that receives the count of credentials.


### -param pdwDefault [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that receives the index of the credential to be used as the default. If no default value has been set, this value should be set to <b>CREDENTIAL_PROVIDER_NO_DEFAULT</b>.


### -param pbAutoLogonWithDefault [out]

Type: <b>BOOL*</b>

A pointer to a <b>BOOL</b> value indicating if the default credential identified by <i>pdwDefault</i> should be used for an auto logon attempt. An auto logon attempt means the Logon UI or Credential UI will immediately call <a href="https://msdn.microsoft.com/c5f7ba25-c38a-431a-b4ad-0e2409f763a3">GetSerialization</a> on the provider's default tile.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required.

When a Logon UI or Credential UI is ready for user interaction, a default credential is selected by default. Since each credential provider supplies a default credential, the following rules determine if <i>pdwDefault</i> will receive focus or if the credential will be automatically logged in.

<ul>
<li>If a default credential has already been specified, that credential is not intended to be used for auto logon, and the <i>pdwDefault</i> is used for auto logon, then <i>pdwDefault</i> will be used as the default.</li>
<li>If <i>pdwDefault</i> is from the last logged on provider and there isn't already a default with auto logon, then <i>pdwDefault</i> will be used as the default.</li>
<li>If no default has been specified, then <i>pdwDefault</i> will be used as the default.</li>
</ul>
If the number of valid credentials change, the credential provider should call <a href="https://msdn.microsoft.com/bff835ed-01b9-4620-a97c-c64a2445e02a">CredentialsChanged</a> on the  <a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a> instance provided in <a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">Advise</a>.

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>


