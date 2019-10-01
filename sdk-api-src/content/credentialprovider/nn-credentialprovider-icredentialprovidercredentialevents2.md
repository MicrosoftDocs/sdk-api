---
UID: NN:credentialprovider.ICredentialProviderCredentialEvents2
title: ICredentialProviderCredentialEvents2 (credentialprovider.h)
author: windows-sdk-content
description: Extends the ICredentialProviderCredentialEvents interface by adding methods that enable batch updating of fields in theLogon UI or Credential UI.
old-location: shell\ICredentialProviderCredentialEvents2.htm
tech.root: shell
ms.assetid: 47290FF7-1785-4470-B3A9-F35C5028A6FE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents2, ICredentialProviderCredentialEvents2 interface [Windows Shell], ICredentialProviderCredentialEvents2 interface [Windows Shell],described, credentialprovider/ICredentialProviderCredentialEvents2, shell.ICredentialProviderCredentialEvents2
ms.topic: interface
f1_keywords: 
 - "credentialprovider/ICredentialProviderCredentialEvents2"
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
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
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialEvents2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredentialEvents2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> interface by adding methods that enable batch updating of fields in theLogon UI or Credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredentialEvents2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>. <b>ICredentialProviderCredentialEvents2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderCredentialEvents2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-beginfieldupdates">BeginFieldUpdates</a>
</td>
<td align="left" width="63%">
Starts a batch update to fields in the logon or credential UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-endfieldupdates">EndFieldUpdates</a>
</td>
<td align="left" width="63%">
Finishes and commits the batch updates started by <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-beginfieldupdates">BeginFieldUpdates</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions">SetFieldOptions</a>
</td>
<td align="left" width="63%">
Specifies whether a specified field in the logon or credential UI should display a "password reveal" glyph or is expected to receive an e-mail address.

</td>
</tr>
</table> 


## -remarks



In Windows 7 and Windows Vista, many credential providers used <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialproviderevents-credentialschanged">ICredentialProviderEvents::CredentialsChanged</a> to update UI. While this works, it causes a re-enumeration of all the credentials from the calling credential provider. The processing of this event can, under some circumstances, lead to flashing or focus changes in the UI due to this re-enumeration. Therefore, using <b>ICredentialProviderEvents::CredentialsChanged</b> solely for UI updates is discouraged. The new recommendation is as follows:

                

<ul>
<li>Use <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialproviderevents-credentialschanged">ICredentialProviderEvents::CredentialsChanged</a> only if a credential provider needs to do automatically logon a user or change the number of credentials it is enumerating.</li>
<li>Use <b>ICredentialProviderCredentialEvents2</b> to update a credential provider's UI.</li>
</ul>
<b>ICredentialProviderCredentialEvents2</b> includes all of the methods inherited from <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>. This includes all of the inherited methods except <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-oncreatingwindow">OnCreatingWindow</a>.

When interacting with a background thread, the use of <b>ICredentialProviderCredentialEvents2</b> is similar to the use of <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>, in that proper inter-thread communication methods must be used.

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Third-parties do not implement this interface. Call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method on <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> to obtain this object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>
 

 

