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

# NET_FW_AUTHENTICATE_TYPE_ enumeration


## -description


The <b>NET_FW_AUTHENTICATE_TYPE</b> enumerated type specifies the type of authentication which must occur in order for traffic to be allowed..


## -enum-fields




### -field NET_FW_AUTHENTICATE_NONE

No security check is performed.


### -field NET_FW_AUTHENTICATE_NO_ENCAPSULATION

The traffic is allowed if it is IPsec-protected with authentication and no encapsulation protection. This means that the peer is authenticated, but there is no integrity protection on the data.


### -field NET_FW_AUTHENTICATE_WITH_INTEGRITY

The traffic is allowed if it is IPsec-protected with authentication and integrity protection.


### -field NET_FW_AUTHENTICATE_AND_NEGOTIATE_ENCRYPTION

The traffic is allowed if its is IPsec-protected with authentication and integrity protection. In addition, negotiation of encryption protections on subsequent packets is requested.


### -field NET_FW_AUTHENTICATE_AND_ENCRYPT

The traffic is allowed if it is IPsec-protected with authentication, integrity and encryption protection since the very first packet. 


## -see-also




<a href="https://msdn.microsoft.com/3efb3491-f030-4a0a-bfbd-ab18fd424a38">INetFwRule3::SecureFlags </a>
 

 

