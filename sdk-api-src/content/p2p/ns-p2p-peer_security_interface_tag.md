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

# peer_security_interface_tag structure


## -description


The <b>PEER_SECURITY_INTERFACE</b> structure specifies the security interfaces that calls to Peer Graphing APIs use to validate, secure, and free records.  Additionally, it allows an application to specify the path to the .DLL that contains an implementation of a security service provider (SSP).


## -struct-fields




### -field dwSize

Specifies the size of the structure. Set the value to   sizeof(<b>PEER_SECURITY_INTERFACE</b>). This member is required and has no default value.


### -field pwzSspFilename

Specifies the full path and file name of a .DLL that  implements the SSP interface. See the <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">SSPI documentation</a> for further information on the SSP interface.


### -field pwzPackageName

Specifies the ID of the security module in the SSP to use.


### -field cbSecurityInfo

Specifies the byte count of the <b>pbSecurityInfo</b> member.	This member is not required if <b>pbSecurityInfo</b> is <b>NULL</b>.  However, if <b>pbSecurityInfo</b> is not <b>NULL</b>, this member must have a value.


### -field pbSecurityInfo

Pointer to a buffer that contains the information  used to create or open a peer graph. This member is optional and can be <b>NULL</b>.

The security data blob pointed to by <b>pbSecurityInfo</b> is  copied and then passed to the SSPI function call of <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">AcquireCredentialsHandle</a>. 


### -field pvContext

Pointer to the security context. This security context is then passed as the first parameter to <a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">PFNPEER_VALIDATE_RECORD</a>, <a href="https://msdn.microsoft.com/aa340e32-6d7f-4218-b120-8c352fdbda0f">PFNPEER_FREE_SECURITY_DATA</a>, and <a href="https://msdn.microsoft.com/454b40f6-a7de-4b59-ae35-a809c4510133">PFNPEER_SECURE_RECORD</a>. This member is optional and can be <b>NULL</b>.


### -field pfnValidateRecord

Pointer to a callback function that is called when a record requires validation. This member is optional and can be <b>NULL</b>. If <b>pfnSecureRecord</b> is <b>NULL</b>, this member must also be <b>NULL</b>.


### -field pfnSecureRecord

Pointer to a callback function that is called when a record must be secured. This member is optional and can be <b>NULL</b>. If <b>pfnValidateRecord</b> is <b>NULL</b>, this member must also be <b>NULL</b>.


### -field pfnFreeSecurityData

Pointer to a callback function used to free any data allocated by the callback pointed to by <b>pfnSecureRecord</b>. This member is optional and can be <b>NULL</b>.


### -field pfnAuthFailed

 




## -remarks



If you have developed your own SSP, your application must not call the Peer Graphing API to access data in the graphing database; doing so can lead to a deadlock situation.  Instead, the application should look at a cached copy of the information.




## -see-also




<a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">AcquireCredentialsHandle</a>



<a href="https://msdn.microsoft.com/aa340e32-6d7f-4218-b120-8c352fdbda0f">PFNPEER_FREE_SECURITY_DATA</a>



<a href="https://msdn.microsoft.com/454b40f6-a7de-4b59-ae35-a809c4510133">PFNPEER_SECURE_RECORD</a>



<a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">PFNPEER_VALIDATE_RECORD</a>



<a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>



<a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>
 

 

