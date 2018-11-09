---
UID: NF:credentialprovider.ICredentialProvider.SetSerialization
title: ICredentialProvider::SetSerialization
author: windows-sdk-content
description: Sets the serialization characteristics of the credential provider.
old-location: shell\ICredentialProvider_SetSerialization.htm
tech.root: shell
ms.assetid: eeeaa3b8-ad0f-4d31-bdd1-646b0e33b7cd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICredentialProvider interface [Windows Shell],SetSerialization method, ICredentialProvider.SetSerialization, ICredentialProvider::SetSerialization, SetSerialization, SetSerialization method [Windows Shell], SetSerialization method [Windows Shell],ICredentialProvider interface, _shell_ICredentialProvider_SetSerialization, credentialprovider/ICredentialProvider::SetSerialization, shell.ICredentialProvider_SetSerialization
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
 - ICredentialProvider.SetSerialization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProvider::SetSerialization


## -description


Sets the serialization characteristics of the credential provider.


## -parameters




### -param pcpcs [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure that stores the serialization characteristics of the credential provider.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required. It accepts a credential and determines if <i>pcpcs</i> was a partial or a full credential. If it is a partial credential, it is either incomplete or was passed for the purpose of displaying some information to the user. If it is a full credential, it should be serialized and submitted. Use the members of the <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> and the flags passed in <a href="https://msdn.microsoft.com/en-us/library/Bb776044(v=VS.85).aspx">SetUsageScenario</a> to determine how to handle the input. The responsibility is on the credential provider to verify the integrity of the input. The Credential UI and Logon UI do not perform any checks on the structure before passing it to the credential provider.

<b>SetSerialization</b> is always called after <a href="https://msdn.microsoft.com/en-us/library/Bb776044(v=VS.85).aspx">SetUsageScenario</a>. The Logon UI also calls <b>SetSerialization</b> when a filter returns a credential through <a href="https://msdn.microsoft.com/en-us/library/Bb776005(v=VS.85).aspx">UpdateRemoteCredential</a>. It does not use this method when re-enumerating tiles because of a call to <a href="https://msdn.microsoft.com/en-us/library/Bb776006(v=VS.85).aspx">CredentialsChanged</a>. The Credential UI calls <b>SetSerialization</b> when an input credential has been suppled by an application.

The Credential UI enforces the following rules based on the <i>dwFlags</i> for this content provider instance defined when <a href="https://msdn.microsoft.com/en-us/library/Bb776044(v=VS.85).aspx">SetUsageScenario</a> was called.

<ul>
<li>If the flags include <b>CREDUIWIN_IN_CRED_ONLY</b>, all credential providers returning <b>S_OK</b> are enabled.</li>
<li>If the flags include <b>CREDUIWIN_AUTHPACKAGE_ONLY</b>, all credential providers returning a success status are enabled.</li>
<li>If neither of those flags are included, then the Credential UI follows the same logic as the Logon UI and all credential providers that implement the <a href="https://msdn.microsoft.com/en-us/library/Bb762493(v=VS.85).aspx">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a><b>CPUS_REDUI</b> will be enabled regardless of the returned status value.</li>
</ul>
Credential providers that implement a <a href="https://msdn.microsoft.com/en-us/library/Bb762493(v=VS.85).aspx">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> of <b>CPUS_LOGON</b> and return a failure from this method will still be enabled.



