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

# tagDOT11_ADHOC_CONNECT_FAIL_REASON enumeration


## -description


Specifies the reason why a connection attempt failed. 


## -enum-fields




### -field DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH

The local host's configuration is incompatible with the target network. This occurs when the local host is 802.11d compliant and the regulatory domain of the local host is not compatible with the regulatory domain of the target network. For more information about regulatory domains, see the IEEE 802.11d-2001 standard. The standard can be downloaded from the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83977">IEEE website</a>.


### -field DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH

The passphrase supplied to authenticate the local machine or user on the target network is incorrect.


### -field DOT11_ADHOC_CONNECT_FAIL_OTHER

The connection failed for another reason.

