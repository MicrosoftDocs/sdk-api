---
UID: NN:credentialprovider.ICredentialProviderCredentialEvents
title: ICredentialProviderCredentialEvents
author: windows-sdk-content
description: Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI.
old-location: shell\ICredentialProviderCredentialEvents.htm
tech.root: shell
ms.assetid: 258449a4-78e2-475e-ab16-6481207e7354
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ICredentialProviderCredentialEvents, ICredentialProviderCredentialEvents interface [Windows Shell], ICredentialProviderCredentialEvents interface [Windows Shell],described, credentialprovider/ICredentialProviderCredentialEvents, shell.ICredentialProviderCredentialEvents, shell_ICredentialProviderCredentialEvents
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents interface


## -description


Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredentialEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICredentialProviderCredentialEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3d434b2c-29be-4301-9271-89688ec8d048">AppendFieldComboBoxItem</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a combo box needs an item appended and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d871480-4424-4a5b-8650-0211bad8b09a">DeleteFieldComboBoxItem</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that an item should be deleted from a combo box and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae3cf911-991d-4363-985a-746846e3c08a">OnCreatingWindow</a>
</td>
<td align="left" width="63%">
Called when the window is created. Enables credentials to retrieve the HWND of the parent window after <a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">Advise</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/860407bd-774a-409f-b7db-e30a964cf879">SetFieldBitmap</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a tile image  field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2d5e08f-6a23-4633-beef-8507ab66b102">SetFieldCheckbox</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a checkbox field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79d66546-8553-4b70-9fe6-aa1b95c1cf25">SetFieldComboBoxSelectedItem</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that the selected item in a combo box has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/649f0f65-78dd-4232-b471-9a18d1448f1d">SetFieldInteractiveState</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3498bca-cc31-4a80-9f31-e1e6d020d777">SetFieldState</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that a field state has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f391177a-0652-4a94-b31c-111fb82c371a">SetFieldString</a>
</td>
<td align="left" width="63%">
Communicates to the Logon UI or Credential UI that the string associated with a field has changed and that the UI should be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a39d67d7-b34d-482b-bfe1-db1f9cdc8d30">SetFieldSubmitButton</a>
</td>
<td align="left" width="63%">
Enables credentials to set the field that the submit button appears adjacent to.

</td>
</tr>
</table> 


## -remarks



These methods should only be called by a credential passing <b>this</b> as the first parameter. Behavior is undefined if you attempt to call these methods using a credential other than the one activated by the call on <a href="https://msdn.microsoft.com/26db5ec5-78bf-4d88-90af-c822c8d3ce45">Advise</a>. If a credential provider has information on another thread and wants to communicate through that thread's Logon UI or Credential UI, the requests will need to go through the credential that received the <b>Advise</b> call.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Third parties do not implement <b>ICredentialProviderCredentialEvents</b>. An implementation is included with Windows.




## -see-also




<a href="https://msdn.microsoft.com/BCF69196-D4E4-41D0-B372-5000FD50164B">Credential Providers in Windows 10</a>



<a href="https://msdn.microsoft.com/26db5ec5-78bf-4d88-90af-c822c8d3ce45">ICredentialProviderCredential::Advise</a>



<a href="https://msdn.microsoft.com/29e01ef4-3186-4f9a-9898-b7424bba2b61">ICredentialProviderCredential::UnAdvise</a>



<a href="https://msdn.microsoft.com/47290FF7-1785-4470-B3A9-F35C5028A6FE">ICredentialProviderCredentialEvents2</a>
 

 

