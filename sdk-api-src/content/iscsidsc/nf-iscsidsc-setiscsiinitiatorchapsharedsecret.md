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

# SetIScsiInitiatorCHAPSharedSecret function


## -description


The <b>SetIscsiInitiatorCHAPSharedSecret</b> function establishes the default Challenge Handshake Authentication Protocol (CHAP) shared secret for all initiators on the computer.



## -parameters




### -param SharedSecretLength [in]

The size, in bytes, of the shared secret contained by the buffer specified by <i>SharedSecret</i>. The shared secret must be at least 96 bits (12 bytes) for non-IPsec connections, at least 8 bits (1 byte) for IPsec connections, and less than 128 bits (16 bytes) for all connection types.


### -param SharedSecret [in]

The buffer that contains the shared secret.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



When an initiator attempts to log in to a target, the initiator can issue a challenge if mutual CHAP is used. The target must respond to the challenge with the initiator CHAP shared secret.

The <b>SetIscsiInitiatorCHAPSharedSecret</b> function specifies the default CHAP secret that all initiators on the computer use to authenticate a target when performing mutual CHAP. Management software can specify the CHAP secret for the initiator to provide when challenged by the target when the initiator calls the <a href="https://msdn.microsoft.com/e94e72d2-b93c-41f4-aafc-78e6a97d7a26">LoginIscsiTarget</a> or <a href="https://msdn.microsoft.com/81f5ac9a-debb-4fa3-8ccf-1303cd45f1de">AddIscsiStaticTarget</a> function.




## -see-also




<a href="https://msdn.microsoft.com/81f5ac9a-debb-4fa3-8ccf-1303cd45f1de">AddIscsiStaticTarget</a>



<a href="https://msdn.microsoft.com/e94e72d2-b93c-41f4-aafc-78e6a97d7a26">LoginIscsiTarget</a>
 

 

