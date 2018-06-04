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

# IMFNetCredentialCache::GetCredential


## -description



Retrieves the credential object for the specified URL.




## -parameters




### -param pszUrl [in]

A null-terminated wide-character string containing the URL for which the credential is needed.


### -param pszRealm [in]

A null-terminated wide-character string containing the realm for the authentication.


### -param dwAuthenticationFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/4a2f5537-b78c-49a6-9b66-d3ca34c3fc67">MFNetAuthenticationFlags</a> enumeration.


### -param ppCred [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/d202e7bc-9ce0-4861-8552-5a4d599b1661">IMFNetCredential</a> interface. The caller must release the interface.


### -param pdwRequirementsFlags






#### - pdwFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/9257d1d7-7ccb-4172-82f0-3694ebb9d487">MFNetCredentialRequirements</a> enumeration.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d02e26e7-e99c-4be7-8495-830eff2f1554">IMFNetCredentialCache</a>
 

 

