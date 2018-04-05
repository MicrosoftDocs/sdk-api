---
UID: NS:ntsecapi._KERB_SMART_CARD_UNLOCK_LOGON
title: "_KERB_SMART_CARD_UNLOCK_LOGON"
author: windows-driver-content
description: Contains information used to unlock a workstation that has been locked during a smart card logon session.
old-location: security\kerb_smart_card_unlock_logon.htm
old-project: SecAuthN
ms.assetid: 5fcd61f6-d93d-4047-b472-8b44f9681907
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PKERB_SMART_CARD_UNLOCK_LOGON, KERB_SMART_CARD_UNLOCK_LOGON, KERB_SMART_CARD_UNLOCK_LOGON structure [Security], PKERB_SMART_CARD_UNLOCK_LOGON, PKERB_SMART_CARD_UNLOCK_LOGON structure pointer [Security], _KERB_SMART_CARD_UNLOCK_LOGON, ntsecapi/KERB_SMART_CARD_UNLOCK_LOGON, ntsecapi/PKERB_SMART_CARD_UNLOCK_LOGON, security.kerb_smart_card_unlock_logon"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KERB_SMART_CARD_UNLOCK_LOGON, *PKERB_SMART_CARD_UNLOCK_LOGON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	KERB_SMART_CARD_UNLOCK_LOGON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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
 

 

