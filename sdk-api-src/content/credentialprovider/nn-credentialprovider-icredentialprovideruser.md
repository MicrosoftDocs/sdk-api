---
UID: NN:credentialprovider.ICredentialProviderUser
title: ICredentialProviderUser
author: windows-sdk-content
description: Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI.
old-location: shell\ICredentialProviderUser.htm
tech.root: shell
ms.assetid: 8EE5FA54-E20E-4d24-AD73-2AE1F0090950
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ICredentialProviderUser, ICredentialProviderUser interface [Windows Shell], ICredentialProviderUser interface [Windows Shell],described, credentialprovider/ICredentialProviderUser, shell.ICredentialProviderUser
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
 - ICredentialProviderUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderUser interface


## -description


Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderUser</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICredentialProviderUser</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderUser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706928(v=VS.85).aspx">GetProviderID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the account provider for this user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706929(v=VS.85).aspx">GetSid</a>
</td>
<td align="left" width="63%">
Retrieves the user's SID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706930(v=VS.85).aspx">GetStringValue</a>
</td>
<td align="left" width="63%">
Retrieves string properties from the <b>ICredentialProviderUser</b> object based on the input value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706931(v=VS.85).aspx">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves a specified property value set for the user.

</td>
</tr>
</table> 


## -remarks



Windows 8 introduces the ability to group credential providers by user. The logon UI can display a set of users rather than a set of multiple credential providers for each user. Selecting a user then displays the individual credential provider options associated with that user.

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Third-parties do not implement this interface. An implementation is included with Windows.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=253508">Credential Provider Framework Changes in Windows 8.docx</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706920(v=VS.85).aspx">ICredentialProviderSetUserArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706923(v=VS.85).aspx">ICredentialProviderUserArray</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

