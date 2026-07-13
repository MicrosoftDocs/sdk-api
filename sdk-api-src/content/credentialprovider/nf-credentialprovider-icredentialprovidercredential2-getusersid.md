---
UID: NF:credentialprovider.ICredentialProviderCredential2.GetUserSid
title: ICredentialProviderCredential2::GetUserSid (credentialprovider.h)
description: Retrieves the security identifier (SID) of the user that is associated with this credential.
helpviewer_keywords: ["GetUserSid","GetUserSid method [Windows Shell]","GetUserSid method [Windows Shell]","ICredentialProviderCredential2 interface","ICredentialProviderCredential2 interface [Windows Shell]","GetUserSid method","ICredentialProviderCredential2.GetUserSid","ICredentialProviderCredential2::GetUserSid","credentialprovider/ICredentialProviderCredential2::GetUserSid","shell.ICredentialProviderCredential2_GetUserSid"]
old-location: shell\ICredentialProviderCredential2_GetUserSid.htm
tech.root: shell
ms.assetid: 8BCB9019-40C0-4026-B3C9-ECA02B9AC871
ms.date: 12/05/2018
ms.keywords: GetUserSid, GetUserSid method [Windows Shell], GetUserSid method [Windows Shell],ICredentialProviderCredential2 interface, ICredentialProviderCredential2 interface [Windows Shell],GetUserSid method, ICredentialProviderCredential2.GetUserSid, ICredentialProviderCredential2::GetUserSid, credentialprovider/ICredentialProviderCredential2::GetUserSid, shell.ICredentialProviderCredential2_GetUserSid
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
 - ICredentialProviderCredential2::GetUserSid
 - credentialprovider/ICredentialProviderCredential2::GetUserSid
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
 - ICredentialProviderCredential2.GetUserSid
---

# ICredentialProviderCredential2::GetUserSid


## -description

Retrieves the security identifier (SID) of the user that is associated with this credential.

## -parameters

### -param sid [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the user's SID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Logon UI will use the returned SID from this method to associate the credential tile with a user tile. To associate the credential with the "Other user" user tile in the Logon UI, this method should return <b>S_FALSE</b> and a null SID. The "Other user" tile is normally only valid when the PC is joined to a domain.


#### Examples

The following example shows a sample implementation of this method. It retrieves the user's SID that corresponds to the credential.

The <i>_pszUserSid</i> variable used here is assumed to be a private member of the class, defined outside of this method and set to the user's SID.

The resource pointed to by <i>ppszSid</i> will be freed by the logon UI, so it does not need to be freed here.

If the user's SID is not available, the method returns <b>S_FALSE</b> with a null SID, which associates the credential with an anonymous user tile. This will cause the tile to appear when the "Other user" tile is selected on a domain-joined PC.


```cpp

// Gets the SID of the user corresponding to the credential. 
HRESULT CSampleCredential::GetUserSid(__deref_out PWSTR *ppszSid) 
{
    *ppszSid = nullptr;
    HRESULT hr = E_UNEXPECTED;

    // _pszUserSid is a private member of CSampleCredential
    if (_pszUserSid != nullptr)
    {
        // ppszSid will be freed by Logon UI
        hr = SHStrDupW(_pszUserSid, ppszSid);
    }
    // Return S_FALSE with a null SID in ppszSid for the
    // credential to be associated with an anonymous user tile.
    else if (_fIsOtherUserTile)
    {
        hr = S_FALSE;
    }

    return hr;
}                     
                    
```

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2">ICredentialProviderCredential2</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getsid">ICredentialProviderUser::GetSid</a>