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

# NET_FW_MODIFY_STATE_ enumeration


## -description


The NET_FW_MODIFY_STATE enumerated type specifies the effect of modifications to the current policy.


## -enum-fields




### -field NET_FW_MODIFY_STATE_OK

Changing or adding a firewall rule or firewall group to the current profile will take effect.


### -field NET_FW_MODIFY_STATE_GP_OVERRIDE

Changing or adding a firewall rule or firewall group to the current profile will not take effect because the profile is controlled by the group policy.


### -field NET_FW_MODIFY_STATE_INBOUND_BLOCKED

Changing or adding a firewall rule or firewall group to the current profile will not take effect because unsolicited inbound traffic is not allowed.


## -see-also




<a href="https://msdn.microsoft.com/72b85ab7-feb4-4bd2-8581-041e2c6d93b1">Windows Firewall with Advanced Security Enumerated Types</a>



<a href="https://msdn.microsoft.com/b1b154f1-2574-4e8e-a088-5e502bb889e7">Windows Firewall with Advanced Security Reference</a>
 

 

