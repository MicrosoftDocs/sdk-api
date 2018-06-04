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

# _KERB_TICKET_PROFILE structure


## -description


The <b>KERB_TICKET_PROFILE</b> structure contains information about an interactive logon profile.
			

This structure is returned by 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


## -struct-fields




### -field Profile


<a href="https://msdn.microsoft.com/8e9dd04b-8155-4f85-be00-ff9d8297deaa">KERB_INTERACTIVE_PROFILE</a> structure containing logon information.


### -field SessionKey


<a href="https://msdn.microsoft.com/ac7ea61c-b1e0-4dc0-931e-81bb6fd74888">KERB_CRYPTO_KEY</a> structure containing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> for the Kerberos ticket.

