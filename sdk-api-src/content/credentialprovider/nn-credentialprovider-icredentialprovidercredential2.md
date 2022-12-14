---
UID: NN:credentialprovider.ICredentialProviderCredential2
title: ICredentialProviderCredential2 (credentialprovider.h)
description: Extends the ICredentialProviderCredential interface by adding a method that retrieves the security identifier (SID) of a user. The credential is associated with that user and can be grouped under the user's tile.
helpviewer_keywords: ["ICredentialProviderCredential2","ICredentialProviderCredential2 interface [Windows Shell]","ICredentialProviderCredential2 interface [Windows Shell]","described","credentialprovider/ICredentialProviderCredential2","shell.ICredentialProviderCredential2"]
old-location: shell\ICredentialProviderCredential2.htm
tech.root: shell
ms.assetid: C1C4BF88-3151-4a8b-A1EE-9616DCB6EA58
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential2, ICredentialProviderCredential2 interface [Windows Shell], ICredentialProviderCredential2 interface [Windows Shell],described, credentialprovider/ICredentialProviderCredential2, shell.ICredentialProviderCredential2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderCredential2
 - credentialprovider/ICredentialProviderCredential2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredential2
---

# ICredentialProviderCredential2 interface


## -description

Extends the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a> interface by adding a method that retrieves the security identifier (SID) of a user. The credential is associated with that user and can be grouped under the user's tile.

## -inheritance

The <b>ICredentialProviderCredential2</b> interface inherits from <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>. <b>ICredentialProviderCredential2</b> also has these types of members:

## -remarks

This class is required for creating a V2 credential provider. V2 credential providers provide a personalized log on experience for the user. This occurs by the credential provider telling the Logon UI what sign in options are available for a user. It is recommended that new credential providers should be V2 credential providers. 

In order to create an <b>ICredentialProviderCredential2</b> instance, a valid SID needs to be returned by the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential2-getusersid">GetUserSid</a> function. Valid is defined by the returned SID being for one of the users currently enumerated by the Logon UI.

A useful tool for getting the available users and determining which ones you want to associate with is the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a> object. This object contains a list of <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a> objects that can be queried to gain information about the users that will be enumerated. For example you could gain the user's SID or username using <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getstringvalue">GetStringValue</a> with a passed in parameter of <b>PKEY_Identity_PrimarySid</b> or <b>PKEY_Identity_USerName</b> respectively. You can even filter the results using <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruserarray-setproviderfilter">SetProviderFilter</a> to only display a subset of available users.

Using the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a> is optional, but it is a convenient way to get the necessary information to make valid SID values. In order to get a list of users that will be enumerated by the Logon UI, implement the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidersetuserarray">ICredentialProviderSetUserArray</a> interface to get the <b>ICredentialProviderUserArray</b> object from <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidersetuserarray-setuserarray">SetUserArray</a>. Logon UI calls <b>SetUserArray</b> before <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-getcredentialcount">GetCredentialCount</a>, so the <b>ICredentialProviderUserArray</b> object is ready when a credential provider is about to return credentials.

A V2 credential provider  is represented by an icon displayed underneath the "Sign-in options" link. In order to provide an icon for your credential provider, define a <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_TYPE</a> of  <b>CPFT_TILE_IMAGE</b> in the credential itself. Then make sure the <i>guidFieldType</i> of the  <a href="/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> is set to <b>CPFG_CREDENTIAL_PROVIDER_LOGO</b>. The recommended size for an icon is 72 by 72 pixels.

Similar to specifying an icon for your credential provider, you can also specify a text string to identify your credential provider. This string appears in a pop-up window when a user hovers over the icon. To do this, define a <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_TYPE</a> of  <b>CPFT_SMALL_TEXT</b> in the credential itself. Then make sure the <i>guidFieldType</i> of the  <a href="/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> is set to <b>CPFG_CREDENTIAL_PROVIDER_LABEL</b>. This string should supplement the credential provider icon described above and be descriptive enough that users understand what it is. For example, the picture password provider's description is "Picture Password".

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface to associate credential tiles with specific user tiles in the Logon UI.

## -see-also

<a href="/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents2">ICredentialProviderCredentialEvents2</a>
