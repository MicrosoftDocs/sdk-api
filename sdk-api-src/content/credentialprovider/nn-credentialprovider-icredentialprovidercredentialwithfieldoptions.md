---
UID: NN:credentialprovider.ICredentialProviderCredentialWithFieldOptions
title: ICredentialProviderCredentialWithFieldOptions
author: windows-sdk-content
description: Provides a method that enables the credential provider framework to determine whether you've made a customization to a field's option in a logon or credential UI.
old-location: shell\ICredentialProviderCredentialWithFieldOptions.htm
tech.root: shell
ms.assetid: 37C391D7-23C2-4053-BC7F-62F8AFD50DA3
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ICredentialProviderCredentialWithFieldOptions, ICredentialProviderCredentialWithFieldOptions interface [Windows Shell], ICredentialProviderCredentialWithFieldOptions interface [Windows Shell],described, credentialprovider/ICredentialProviderCredentialWithFieldOptions, shell.ICredentialProviderCredentialWithFieldOptions
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialWithFieldOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialWithFieldOptions interface


## -description


Provides a method that enables the credential provider framework to determine whether you've made a customization to a field's option in a logon or credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredentialWithFieldOptions</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICredentialProviderCredentialWithFieldOptions</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderCredentialWithFieldOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh706919(v=VS.85).aspx">GetFieldOptions</a>
</td>
<td align="left" width="63%">
Retrieves the current option set for a specified field in a logon or credential UI. Called by the credential provider framework.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface if your credential provider overrides the default field options through <a href="https://msdn.microsoft.com/en-us/library/Hh706917(v=VS.85).aspx">ICredentialProviderCredentialEvents2::SetFieldOptions</a>. This enables the credential provider framework to determine the field options that you've specified .




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

