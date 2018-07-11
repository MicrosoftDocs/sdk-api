---
UID: NN:credentialprovider.ICredentialProvider
title: ICredentialProvider
author: windows-sdk-content
description: Exposes methods used in the setup and manipulation of a credential provider. All credential providers must implement this interface.
old-location: shell\ICredentialProvider.htm
old-project: shell
ms.assetid: 7ce6cd61-16d1-414e-b9b3-4929a65c0cc6
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ICredentialProvider, ICredentialProvider interface [Windows Shell], ICredentialProvider interface [Windows Shell],described, credentialprovider/ICredentialProvider, shell.ICredentialProvider, shell_ICredentialProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProvider interface


## -description


Exposes methods used in the setup and manipulation of a credential provider. All credential providers must implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICredentialProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">Advise</a>
</td>
<td align="left" width="63%">
Allows a credential provider to initiate events in the Logon UI or Credential UI through a callback interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eec370b7-0db8-492f-8dc3-4f391e1a55e7">GetCredentialAt</a>
</td>
<td align="left" width="63%">
Gets a specific credential.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d940d46-d4c2-4ab5-8559-416d78d3579e">GetCredentialCount</a>
</td>
<td align="left" width="63%">
Gets the number of available credentials under this credential provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb9f063d-afbc-4f6b-a4a5-19a9a644f029">GetFieldDescriptorAt</a>
</td>
<td align="left" width="63%">
Gets metadata that describes a specified field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dacaa846-1838-4348-ba63-c204cbe0e2ae">GetFieldDescriptorCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of fields in the needed to display this provider's credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeeaa3b8-ad0f-4d31-bdd1-646b0e33b7cd">SetSerialization</a>
</td>
<td align="left" width="63%">
Sets the serialization characteristics of the credential provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62577b41-e115-45df-9f9b-c5c282365a3e">SetUsageScenario</a>
</td>
<td align="left" width="63%">
Defines the scenarios for which the credential provider is valid. Called whenever the credential provider is initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d971c7be-f440-41ce-945d-4dbe51554e59">UnAdvise</a>
</td>
<td align="left" width="63%">
Used by the Logon UI or Credential UI to advise the credential provider that event callbacks are no longer accepted.

</td>
</tr>
</table> 


## -remarks



This interface is how you will interact with the Logon UI and the Credential UI for your app.

An instantiated credential provider is maintained for the entire lifetime of a Logon UI. Because of this, the Logon UI can maintain the state of a credential provider. In particular, it remembers which provider and tile provided a credential. This means that you can potentially store state information when you are using a <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> of <b>CPUS_LOGON</b>, <b>CPUS_UNLOCK_WORKSTATION</b>, and <b>CPUS_CHANGE_PASSWORD</b>. This is not the case with the Credential UI. The Credential UI creates a new instance of the provider every time an application calls <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a>. Because of this, the Credential UI cannot remember a credential provider's state.

Be aware that  a <a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> generated in one scenario might be saved and used in a subsequent usage scenario. Because of this, it is necessary to make sure your <b>ICredentialProvider</b> implementation is robust enough to handle this scenario.

Windows 8 adds new functionality in the credential providers API, primarily the ability to group credentials by user. For more information, download the Microsoft Word document <a href="http://go.microsoft.com/fwlink/p/?linkid=253508">Credential Provider Framework Changes in Windows 8</a> from the Microsoft Download Center.




## -see-also




<a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a>



<a href="http://go.microsoft.com/fwlink/?LinkId=717287">Credential Provider driven Windows Logon Experience</a>



<a href="https://msdn.microsoft.com/BCF69196-D4E4-41D0-B372-5000FD50164B">Credential Providers in Windows 10</a>



<a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>
 

 

