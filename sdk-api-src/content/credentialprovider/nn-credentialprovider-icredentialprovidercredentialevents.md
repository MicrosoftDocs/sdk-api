---
UID: NN:credentialprovider.ICredentialProviderCredentialEvents
title: ICredentialProviderCredentialEvents (credentialprovider.h)
author: windows-sdk-content
description: Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI.
old-location: shell\ICredentialProviderCredentialEvents.htm
tech.root: shell
ms.assetid: 258449a4-78e2-475e-ab16-6481207e7354
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents, ICredentialProviderCredentialEvents interface [Windows Shell], ICredentialProviderCredentialEvents interface [Windows Shell],described, credentialprovider/ICredentialProviderCredentialEvents, shell.ICredentialProviderCredentialEvents, shell_ICredentialProviderCredentialEvents
ms.topic: interface
f1_keywords: 
 - "credentialprovider/ICredentialProviderCredentialEvents"
dev_langs:
 - c++
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
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderCredentialEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredentialEvents interface


## -description


Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredentialEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderCredentialEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderCredentialEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-appendfieldcomboboxitem">AppendFieldComboBoxItem</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a combo box needs an item appended and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-deletefieldcomboboxitem">DeleteFieldComboBoxItem</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that an item should be deleted from a combo box and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-oncreatingwindow">OnCreatingWindow</a>
</td>
<td align="left" width="63%">
Called when the window is created. Enables credentials to retrieve the HWND of the parent window after <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-advise">Advise</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldbitmap">SetFieldBitmap</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a tile image  field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldcheckbox">SetFieldCheckbox</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a checkbox field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldcomboboxselecteditem">SetFieldComboBoxSelectedItem</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that the selected item in a combo box has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldinteractivestate">SetFieldInteractiveState</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldstate">SetFieldState</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a field state has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldstring">SetFieldString</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that the string associated with a field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldsubmitbutton">SetFieldSubmitButton</a>
</td>
<td align="left" width="63%">
Enables credentials to set the field that the submit button appears adjacent to.

</td>
</tr>
</table> 


## -remarks



These methods should only be called by a credential passing <b>this</b> as the first parameter. Behavior is undefined if you attempt to call these methods using a credential other than the one activated by the call on <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-advise">Advise</a>. If a credential provider has information on another thread and wants to communicate through that thread's Logon UI or Credential UI, the requests will need to go through the credential that received the <b>Advise</b> call.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Third parties do not implement <b>ICredentialProviderCredentialEvents</b>. An implementation is included with Windows.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-advise">ICredentialProviderCredential::Advise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-unadvise">ICredentialProviderCredential::UnAdvise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents2">ICredentialProviderCredentialEvents2</a>
 

 

