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

# SspiEncodeAuthIdentityAsStrings function


## -description


Encodes the specified authentication identity as three strings.


## -parameters




### -param pAuthIdentity [in]

The credential structure to be encoded.


### -param ppszUserName [out]

The marshaled user name of the identity specified by the <i>pAuthIdentity</i> parameter.

When you have finished using this string, free it by calling the <a href="https://msdn.microsoft.com/6199f66e-7adb-4bb9-8e77-a735e31dd5f6">SspiFreeAuthIdentity</a> function.


### -param ppszDomainName [out]

The marshaled domain name of the identity specified by the <i>pAuthIdentity</i> parameter.

When you have finished using this string, free it by calling the <a href="https://msdn.microsoft.com/6199f66e-7adb-4bb9-8e77-a735e31dd5f6">SspiFreeAuthIdentity</a> function.


### -param ppszPackedCredentialsString [out]

An encoded string version of a <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure that specifies the users credentials.

When you have finished using this string, free it by calling the <a href="https://msdn.microsoft.com/6199f66e-7adb-4bb9-8e77-a735e31dd5f6">SspiFreeAuthIdentity</a> function.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
<dt>0xC000000D</dt>
</dl>
</td>
<td width="60%">
The <b>SEC_WINNT_AUTH_IDENTITY_FLAGS_PROCESS_ENCRYPTED</b> flag is set in the identity  structure specified by the <i>pAuthIdentity</i> parameter.

</td>
</tr>
</table>
 



