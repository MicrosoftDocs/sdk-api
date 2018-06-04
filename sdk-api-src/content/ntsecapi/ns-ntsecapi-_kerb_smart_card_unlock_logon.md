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

# _KERB_SMART_CARD_UNLOCK_LOGON structure


## -description


The <b>KERB_SMART_CARD_UNLOCK_LOGON</b> structure contains information used to unlock a workstation that has been locked during a smart card <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.


## -struct-fields




### -field Logon

A <a href="https://msdn.microsoft.com/1a154034-6a2d-46be-9fb6-7c7d425d12f6">KERB_SMART_CARD_LOGON</a> structure that specifies the smart card logon session. The <b>MessageType</b> member of the <b>KERB_SMART_CARD_LOGON</b> structure must be set to <b>KerbWorkstationUnlockLogon</b>.


### -field LogonId

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure that contains the identity of the user attempting to unlock the workstation.


## -see-also




<a href="https://msdn.microsoft.com/1a154034-6a2d-46be-9fb6-7c7d425d12f6">KERB_SMART_CARD_LOGON</a>
 

 

