---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICredentialProviderCredential2::GetUserSid


## -description


Retrieves the security identifier (SID) of the user that is associated with this credential.


## -parameters




### -param sid [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the user's SID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Logon UI will use the returned SID from this method to associate the credential tile with a user tile. To associate the credential with the "Other user" user tile in the Logon UI, this method should return <b>S_FALSE</b> and a null SID. The "Other user" tile is normally only valid when the PC is joined to a domain.


#### Examples

The following example shows a sample implementation of this method. It retrieves the user's SID that corresponds to the credential.

The <i>_pszUserSid</i> variable used here is assumed to be a private member of the class, defined outside of this method and set to the user's SID.

The resource pointed to by <i>ppszSid</i> will be freed by the logon UI, so it does not need to be freed here.

If the user's SID is not available, the method returns <b>S_FALSE</b> with a null SID, which associates the credential with an anonymous user tile. This will cause the tile to appear when the "Other user" tile is selected on a domain-joined PC.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
                    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/C1C4BF88-3151-4a8b-A1EE-9616DCB6EA58">ICredentialProviderCredential2</a>



<a href="https://msdn.microsoft.com/FDC5D586-D72B-4eb1-BE7C-CFD8E0B48F48">ICredentialProviderUser::GetSid</a>
 

 

