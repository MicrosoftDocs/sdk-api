---
UID: NN:credentialprovider.ICredentialProviderUserArray
title: ICredentialProviderUserArray (credentialprovider.h)
description: Represents the set of users that will appear in the logon or credential UI. This information enables the credential provider to enumerate the set to retrieve property information about each user to populate fields or filter the set.
helpviewer_keywords: ["ICredentialProviderUserArray","ICredentialProviderUserArray interface [Windows Shell]","ICredentialProviderUserArray interface [Windows Shell]","described","credentialprovider/ICredentialProviderUserArray","shell.ICredentialProviderUserArray"]
old-location: shell\ICredentialProviderUserArray.htm
tech.root: shell
ms.assetid: 50FC43C1-B148-4e42-AB38-3559BD056855
ms.date: 12/05/2018
ms.keywords: ICredentialProviderUserArray, ICredentialProviderUserArray interface [Windows Shell], ICredentialProviderUserArray interface [Windows Shell],described, credentialprovider/ICredentialProviderUserArray, shell.ICredentialProviderUserArray
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
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderUserArray
 - credentialprovider/ICredentialProviderUserArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUserArray
---

# ICredentialProviderUserArray interface


## -description

Represents the set of users that will appear in the logon or credential UI. This information enables the credential provider to enumerate the set to retrieve property information about each user to populate fields or filter the set.

## -inheritance

The <b>ICredentialProviderUserArray</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderUserArray</b> also has these types of members:

## -remarks

This object is provided by the Windows credential provider framework to your credential provider through the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidersetuserarray-setuserarray">ICredentialProviderSetUserArray::SetUserArray</a> method. Ownership of this object remains with the credential provider framework.

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Third-parties do not implement this interface. An implementation is included with Windows.


#### Examples

The following example demonstrates a scenario that uses some of the methods of this interface. The <code>pcpua</code> variable represents a previously declared <b>ICredentialProviderUserArray</b> object.


```cpp

DWORD dwCount = 0;

HRESULT hr = pcpua->GetCount(&dwCount);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < dwCount; i++)
    {
        ICredentialProviderUser *pcpu = NULL;
        hr = pcpua->GetAt(i, &pcpu);

        if (SUCCEEDED(hr))
        {
            PWSTR pszName = NULL;
            hr = pcpu->GetStringValue(PKEY_Identity_UserName, &pszName);

            if (SUCCEEDED(hr))
            {
                // Do something with the string
                CoTaskMemFree(pszName);
            }
            pcpu->Release();
        }
    }
}
```

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidersetuserarray">ICredentialProviderSetUserArray</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
