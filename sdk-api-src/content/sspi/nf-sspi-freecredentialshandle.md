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

# FreeCredentialsHandle function


## -description


The <b>FreeCredentialsHandle</b> function notifies the security system that the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> are no longer needed. An application calls this function to free the credential handle acquired in the call to the 
<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a> function after calling the <a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function to free any context handles associated with the credential. When all references to this credential set have been removed, the credentials themselves can be removed.

Failure to free credentials handles will result in memory leaks.


## -parameters




### -param phCredential [in]

A pointer to the <a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CredHandle</a> handle obtained by using the 
<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a> function.


## -returns




						If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle passed to the function is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a>



<a href="authentication_functions.htm">SSPI Functions</a>
 

 

