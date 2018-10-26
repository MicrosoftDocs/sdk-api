---
UID: NN:credentialprovider.ICredentialProviderCredential
title: ICredentialProviderCredential
author: windows-sdk-content
description: Exposes methods that enable the handling of a credential.
old-location: shell\ICredentialProviderCredential.htm
tech.root: shell
ms.assetid: ef9bb148-0b4e-4c13-b69d-3e63a5592e4a
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ICredentialProviderCredential, ICredentialProviderCredential interface [Windows Shell], ICredentialProviderCredential interface [Windows Shell],described, credentialprovider/ICredentialProviderCredential, shell.ICredentialProviderCredential, shell_ICredentialProviderCredential
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
 - ICredentialProviderCredential
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredential interface


## -description


Exposes methods that enable the handling of a credential.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredential</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICredentialProviderCredential</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderCredential</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26db5ec5-78bf-4d88-90af-c822c8d3ce45">Advise</a>
</td>
<td align="left" width="63%">
Enables a credential to initiate events in the Logon UI or Credential UI through a callback interface. This method should be called before other methods in <b>ICredentialProviderCredential</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04e371cb-f968-4a15-9285-e676dff59899">CommandLinkClicked</a>
</td>
<td align="left" width="63%">
Enables the Logon UI and Credential UI to indicate that a link was clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5171b8f4-877b-43ab-be1d-4ccffdfc74ce">GetBitmapValue</a>
</td>
<td align="left" width="63%">
Enables retrieval of bitmap data from a credential with a bitmap field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7fcf44c-bc5e-4d15-bbd8-7f7e9df9240b">GetCheckboxValue</a>
</td>
<td align="left" width="63%">
Retrieves the checkbox value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e64c6b80-03c9-46a3-91bd-6cd67d666540">GetComboBoxValueAt</a>
</td>
<td align="left" width="63%">
Gets the string label for a combo box entry at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50d28ad6-ab18-4648-8e3d-1759ce6b5aeb">GetComboBoxValueCount</a>
</td>
<td align="left" width="63%">
Gets a count of the items in the specified combo box and designates which item should have initial selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a709835-cf89-464d-a257-d16a1312ab44">GetFieldState</a>
</td>
<td align="left" width="63%">
Retrieves the field state. The Logon UI and Credential UI use this to gain information about a field of a credential to display this information in the user tile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5f7ba25-c38a-431a-b4ad-0e2409f763a3">GetSerialization</a>
</td>
<td align="left" width="63%">
Called in response to an attempt to submit this credential to the underlying authentication engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b891c735-9822-4bc1-a1cc-0c50b35c03c4">GetStringValue</a>
</td>
<td align="left" width="63%">
Enables retrieval of text from a credential with a text field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74adc133-aa4d-405f-a98d-c9cfc719648a">GetSubmitButtonValue</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of a field that the submit button should be placed next to in the Logon UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13d6dda7-4a4f-45bf-af91-72f80497b9f7">ReportResult</a>
</td>
<td align="left" width="63%">
Translates a received error status code into the appropriate user-readable message.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7da8e80f-1cbe-4a10-96a0-7eb6e61b0f9b">SetCheckboxValue</a>
</td>
<td align="left" width="63%">
Enables a Logon UI and Credential UI ro indicate that a checkbox value has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe33500b-ab34-4f28-b244-692e62d6d30c">SetComboBoxSelectedValue</a>
</td>
<td align="left" width="63%">
Enables a Logon UI and Credential UI to indicate that a combo box value has been selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89c01b7c-0d22-44f8-9934-b01d7410f85f">SetDeselected</a>
</td>
<td align="left" width="63%">
Called when a credential loses selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06a0482c-100c-445f-9a77-279d85492f42">SetSelected</a>
</td>
<td align="left" width="63%">
Called when a credential is selected. Enables the implementer to set logon characteristics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea2007b9-fff1-4cd2-8656-61ec050a8e96">SetStringValue</a>
</td>
<td align="left" width="63%">
Enables a Logon UI or Credential UI to update the text for a <b>CPFT_EDIT_TEXT</b> fields as the user types in them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29e01ef4-3186-4f9a-9898-b7424bba2b61">UnAdvise</a>
</td>
<td align="left" width="63%">
Used by the Logon UI or Credential UI to advise the credential that event callbacks are no longer accepted.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>ICredentialProviderCredential</b> is implemented by outside parties providing a Logon UI or Credential UI  prompting for user credentials. Enumeration of user tiles cannot be done without an implementation of this interface.

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/BCF69196-D4E4-41D0-B372-5000FD50164B">Credential Providers in Windows 10</a>



<a href="https://msdn.microsoft.com/7ce6cd61-16d1-414e-b9b3-4929a65c0cc6">ICredentialProvider</a>
 

 

