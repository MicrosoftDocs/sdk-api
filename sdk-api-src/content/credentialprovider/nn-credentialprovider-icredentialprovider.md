---
UID: NN:credentialprovider.ICredentialProvider
title: ICredentialProvider
author: windows-sdk-content
description: Exposes methods used in the setup and manipulation of a credential provider. All credential providers must implement this interface.
old-location: shell\ICredentialProvider.htm
tech.root: shell
ms.assetid: 7ce6cd61-16d1-414e-b9b3-4929a65c0cc6
ms.author: windowssdkdev
ms.date: 09/19/2018
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
 - ICredentialProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProvider interface


## -description


Exposes methods used in the setup and manipulation of a credential provider. All credential providers must implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICredentialProvider</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb776037(v=VS.85).aspx">Advise</a>
</td>
<td align="left" width="63%">
Allows a credential provider to initiate events in the Logon UI or Credential UI through a callback interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776038(v=VS.85).aspx">GetCredentialAt</a>
</td>
<td align="left" width="63%">
Gets a specific credential.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776039(v=VS.85).aspx">GetCredentialCount</a>
</td>
<td align="left" width="63%">
Gets the number of available credentials under this credential provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776040(v=VS.85).aspx">GetFieldDescriptorAt</a>
</td>
<td align="left" width="63%">
Gets metadata that describes a specified field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776041(v=VS.85).aspx">GetFieldDescriptorCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of fields in the needed to display this provider's credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776043(v=VS.85).aspx">SetSerialization</a>
</td>
<td align="left" width="63%">
Sets the serialization characteristics of the credential provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776044(v=VS.85).aspx">SetUsageScenario</a>
</td>
<td align="left" width="63%">
Defines the scenarios for which the credential provider is valid. Called whenever the credential provider is initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776045(v=VS.85).aspx">UnAdvise</a>
</td>
<td align="left" width="63%">
Used by the Logon UI or Credential UI to advise the credential provider that event callbacks are no longer accepted.

</td>
</tr>
</table> 


## -remarks



This interface is how you will interact with the Logon UI and the Credential UI for your app.

An instantiated credential provider is maintained for the entire lifetime of a Logon UI. Because of this, the Logon UI can maintain the state of a credential provider. In particular, it remembers which provider and tile provided a credential. This means that you can potentially store state information when you are using a <a href="https://msdn.microsoft.com/en-us/library/Bb762493(v=VS.85).aspx">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> of <b>CPUS_LOGON</b>, <b>CPUS_UNLOCK_WORKSTATION</b>, and <b>CPUS_CHANGE_PASSWORD</b>. This is not the case with the Credential UI. The Credential UI creates a new instance of the provider every time an application calls <a href="https://msdn.microsoft.com/en-us/library/Aa375178(v=VS.85).aspx">CredUIPromptForWindowsCredentials</a>. Because of this, the Credential UI cannot remember a credential provider's state.

Be aware that  a <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> generated in one scenario might be saved and used in a subsequent usage scenario. Because of this, it is necessary to make sure your <b>ICredentialProvider</b> implementation is robust enough to handle this scenario.

Windows 8 adds new functionality in the credential providers API, primarily the ability to group credentials by user. For more information, download the Microsoft Word document <a href="http://go.microsoft.com/fwlink/p/?linkid=253508">Credential Provider Framework Changes in Windows 8</a> from the Microsoft Download Center.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762493(v=VS.85).aspx">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a>



<a href="http://go.microsoft.com/fwlink/?LinkId=717287">Credential Provider driven Windows Logon Experience</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt158211(v=VS.85).aspx">Credential Providers in Windows 10</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776029(v=VS.85).aspx">ICredentialProviderCredential</a>
 

 

