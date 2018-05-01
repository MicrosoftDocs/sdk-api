---
UID: NN:credentialprovider.ICredentialProviderUser
title: ICredentialProviderUser
author: windows-driver-content
description: Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI.
old-location: shell\ICredentialProviderUser.htm
old-project: shell
ms.assetid: 8EE5FA54-E20E-4d24-AD73-2AE1F0090950
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ICredentialProviderUser, ICredentialProviderUser interface [Windows Shell], ICredentialProviderUser interface [Windows Shell], described, credentialprovider/ICredentialProviderUser, shell.ICredentialProviderUser
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Authui.dll
api_name:
-	ICredentialProviderUser
product: Windows
targetos: Windows
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
---

# ICredentialProviderUser interface


## -description


Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderUser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICredentialProviderUser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/7BD6C532-0266-4579-96FA-91D0AF7E6C4C">GetProviderID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the account provider for this user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FDC5D586-D72B-4eb1-BE7C-CFD8E0B48F48">GetSid</a>
</td>
<td align="left" width="63%">
Retrieves the user's SID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597621">GetStringValue</a>
</td>
<td align="left" width="63%">
Retrieves string properties from the <b>ICredentialProviderUser</b> object based on the input value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
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



<a href="https://msdn.microsoft.com/85422EF5-8A8E-4e14-BD32-953C31A9D401">ICredentialProviderSetUserArray</a>



<a href="https://msdn.microsoft.com/50FC43C1-B148-4e42-AB38-3559BD056855">ICredentialProviderUserArray</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

