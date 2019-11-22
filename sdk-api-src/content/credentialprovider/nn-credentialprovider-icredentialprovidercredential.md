---
UID: NN:credentialprovider.ICredentialProviderCredential
title: ICredentialProviderCredential (credentialprovider.h)

description: Exposes methods that enable the handling of a credential.
old-location: shell\ICredentialProviderCredential.htm
tech.root: shell
ms.assetid: ef9bb148-0b4e-4c13-b69d-3e63a5592e4a

ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential, ICredentialProviderCredential interface [Windows Shell], ICredentialProviderCredential interface [Windows Shell],described, credentialprovider/ICredentialProviderCredential, shell.ICredentialProviderCredential, shell_ICredentialProviderCredential
ms.topic: interface
f1_keywords: 
 - "credentialprovider/ICredentialProviderCredential"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredential interface


## -description


Exposes methods that enable the handling of a credential.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredential</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderCredential</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-advise">Advise</a>
</td>
<td align="left" width="63%">
Enables a credential to initiate events in the Logon UI or Credential UI through a callback interface. This method should be called before other methods in <b>ICredentialProviderCredential</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-commandlinkclicked">CommandLinkClicked</a>
</td>
<td align="left" width="63%">
Enables the Logon UI and Credential UI to indicate that a link was clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getbitmapvalue">GetBitmapValue</a>
</td>
<td align="left" width="63%">
Enables retrieval of bitmap data from a credential with a bitmap field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getcheckboxvalue">GetCheckboxValue</a>
</td>
<td align="left" width="63%">
Retrieves the checkbox value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getcomboboxvalueat">GetComboBoxValueAt</a>
</td>
<td align="left" width="63%">
Gets the string label for a combo box entry at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getcomboboxvaluecount">GetComboBoxValueCount</a>
</td>
<td align="left" width="63%">
Gets a count of the items in the specified combo box and designates which item should have initial selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getfieldstate">GetFieldState</a>
</td>
<td align="left" width="63%">
Retrieves the field state. The Logon UI and Credential UI use this to gain information about a field of a credential to display this information in the user tile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getserialization">GetSerialization</a>
</td>
<td align="left" width="63%">
Called in response to an attempt to submit this credential to the underlying authentication engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getstringvalue">GetStringValue</a>
</td>
<td align="left" width="63%">
Enables retrieval of text from a credential with a text field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getsubmitbuttonvalue">GetSubmitButtonValue</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of a field that the submit button should be placed next to in the Logon UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-reportresult">ReportResult</a>
</td>
<td align="left" width="63%">
Translates a received error status code into the appropriate user-readable message.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-setcheckboxvalue">SetCheckboxValue</a>
</td>
<td align="left" width="63%">
Enables a Logon UI and Credential UI ro indicate that a checkbox value has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-setcomboboxselectedvalue">SetComboBoxSelectedValue</a>
</td>
<td align="left" width="63%">
Enables a Logon UI and Credential UI to indicate that a combo box value has been selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-setdeselected">SetDeselected</a>
</td>
<td align="left" width="63%">
Called when a credential loses selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-setselected">SetSelected</a>
</td>
<td align="left" width="63%">
Called when a credential is selected. Enables the implementer to set logon characteristics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-setstringvalue">SetStringValue</a>
</td>
<td align="left" width="63%">
Enables a Logon UI or Credential UI to update the text for a <b>CPFT_EDIT_TEXT</b> fields as the user types in them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-unadvise">UnAdvise</a>
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
<li>Always securely discard secrets. To do this, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider">ICredentialProvider</a>
 

 

