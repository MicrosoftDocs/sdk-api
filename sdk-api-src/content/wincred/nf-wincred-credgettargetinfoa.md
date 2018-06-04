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

# CredGetTargetInfoA function


## -description



			The <b>CredGetTargetInfo</b> function retrieves all known target name information for the named target computer. This executed locally and does not need any particular privilege. The information returned is expected to be passed to the 
<a href="https://msdn.microsoft.com/b62cb9c9-2a64-4ef4-97f0-e1ea85976d3e">CredReadDomainCredentials</a> and 
<a href="https://msdn.microsoft.com/6b54c14f-a736-4fb0-b4e4-97765a792a5e">CredWriteDomainCredentials</a> functions. The information should not be used for any other purpose.

Authentication packages compute <i>TargetInfo</i> when attempting to authenticate to a <i>TargetName</i>. The authentication packages cache this target information to make it available to <b>CredGetTargetInfo</b>. Therefore, the target information will only be available from a recent attempt to authenticate a <i>TargetName</i>.

Authentication packages not in the LSA process can cache a <i>TargetInfo</i> for later retrieval by <b>CredGetTargetInfo</b> by calling <a href="https://msdn.microsoft.com/b62cb9c9-2a64-4ef4-97f0-e1ea85976d3e">CredReadDomainCredentials</a> with the CRED_CACHE_TARGET_INFORMATION flag.


## -parameters




### -param TargetName [in]

Pointer to a null-terminated string that contains the name of the target computer for which information is to be retrieved.


### -param Flags [in]

Flags controlling the operation of the function. The following flag can be used: 




CRED_ALLOW_NAME_RESOLUTION

If no target information can be found for <i>TargetName</i> name resolution is done on <i>TargetName</i> to convert it to other forms. If target information exists for any of those other forms, it is returned. Currently only DNS name resolution is done.

This is useful if the application does not call an authentication package directly. The application can pass the <i>TargetName</i> to another layer of software to authenticate to the server, and that layer of software might resolve the name and pass the resolved name to the authentication package. As such, there will be no target information for the original <i>TargetName</i>.


### -param TargetInfo [out]

Pointer to a single allocated block buffer to contain the target information. At least one of the returned members of <i>TargetInfo</i> will be non-NULL. Any pointers contained within the buffer are pointers to locations within this single allocated block. The single returned buffer must be freed by calling <a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>.


## -returns



The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

<ul>
<li>ERROR_NOT_FOUND 


Target information for the named server is not available.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>



<a href="https://msdn.microsoft.com/b62cb9c9-2a64-4ef4-97f0-e1ea85976d3e">CredReadDomainCredentials</a>



<a href="https://msdn.microsoft.com/6b54c14f-a736-4fb0-b4e4-97765a792a5e">CredWriteDomainCredentials</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

