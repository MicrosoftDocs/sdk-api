---
UID: NE:icftypes.NET_FW_MODIFY_STATE_
title: NET_FW_MODIFY_STATE_
author: windows-driver-content
description: Specifies the effect of modifications to the current policy.
old-location: ics\net_fw_modify_state.htm
old-project: ICS
ms.assetid: c9bfe7e8-2668-499f-9b75-3457235655b8
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: NET_FW_MODIFY_STATE, NET_FW_MODIFY_STATE enumeration [ICS/ICF], NET_FW_MODIFY_STATE_, NET_FW_MODIFY_STATE_GP_OVERRIDE, NET_FW_MODIFY_STATE_INBOUND_BLOCKED, NET_FW_MODIFY_STATE_OK, icftypes/NET_FW_MODIFY_STATE, icftypes/NET_FW_MODIFY_STATE_GP_OVERRIDE, icftypes/NET_FW_MODIFY_STATE_INBOUND_BLOCKED, icftypes/NET_FW_MODIFY_STATE_OK, ics.net_fw_modify_state
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: icftypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NET_FW_MODIFY_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Icftypes.h
api_name:
-	NET_FW_MODIFY_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

