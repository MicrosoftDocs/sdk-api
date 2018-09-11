---
UID: NN:credentialprovider.ICredentialProviderUserArray
title: ICredentialProviderUserArray
author: windows-sdk-content
description: Represents the set of users that will appear in the logon or credential UI. This information enables the credential provider to enumerate the set to retrieve property information about each user to populate fields or filter the set.
old-location: shell\ICredentialProviderUserArray.htm
tech.root: shell
ms.assetid: 50FC43C1-B148-4e42-AB38-3559BD056855
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ICredentialProviderUserArray, ICredentialProviderUserArray interface [Windows Shell], ICredentialProviderUserArray interface [Windows Shell],described, credentialprovider/ICredentialProviderUserArray, shell.ICredentialProviderUserArray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUserArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderUserArray interface


## -description


Represents the set of users that will appear in the logon or credential UI. This information enables the credential provider to enumerate the set to retrieve property information about each user to populate fields or filter the set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderUserArray</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICredentialProviderUserArray</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderUserArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706924(v=VS.85).aspx">GetAccountOptions</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the "Other user" tile for local or Microsoft accounts is shown in the logon or credential UI. This information can be used by a credential provider to show the same behavior as the password or Microsoft account provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706925(v=VS.85).aspx">GetAt</a>
</td>
<td align="left" width="63%">
Retrieves a specified user from the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706926(v=VS.85).aspx">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/en-us/library/Hh706922(v=VS.85).aspx">ICredentialProviderUser</a> objects in the user array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706927(v=VS.85).aspx">SetProviderFilter</a>
</td>
<td align="left" width="63%">
Limits the set of users in the array to either local accounts or Microsoft accounts.

</td>
</tr>
</table> 


## -remarks



This object is provided by the Windows credential provider framework to your credential provider through the <a href="https://msdn.microsoft.com/en-us/library/Hh706921(v=VS.85).aspx">ICredentialProviderSetUserArray::SetUserArray</a> method. Ownership of this object remains with the credential provider framework.

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




<a href="http://go.microsoft.com/fwlink/p/?linkid=253508">Credential Provider Framework Changes in Windows 8.docx</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706920(v=VS.85).aspx">ICredentialProviderSetUserArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706922(v=VS.85).aspx">ICredentialProviderUser</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

