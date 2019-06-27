---
UID: NE:icftypes.NET_FW_MODIFY_STATE_
title: NET_FW_MODIFY_STATE (icftypes.h)
author: windows-sdk-content
description: Specifies the effect of modifications to the current policy.
old-location: ics\net_fw_modify_state.htm
tech.root: ics
ms.assetid: c9bfe7e8-2668-499f-9b75-3457235655b8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NET_FW_MODIFY_STATE, NET_FW_MODIFY_STATE enumeration [ICS/ICF], NET_FW_MODIFY_STATE_GP_OVERRIDE, NET_FW_MODIFY_STATE_INBOUND_BLOCKED, NET_FW_MODIFY_STATE_OK, icftypes/NET_FW_MODIFY_STATE, icftypes/NET_FW_MODIFY_STATE_GP_OVERRIDE, icftypes/NET_FW_MODIFY_STATE_INBOUND_BLOCKED, icftypes/NET_FW_MODIFY_STATE_OK, ics.net_fw_modify_state
ms.topic: enum
f1_keywords: 
 - "icftypes/NET_FW_MODIFY_STATE"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Icftypes.h
api_name:
 - NET_FW_MODIFY_STATE
product: Windows
targetos: Windows
req.typenames: NET_FW_MODIFY_STATE
req.redist: 
ms.custom: 19H1
---

# NET_FW_MODIFY_STATE enumeration


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-enumerated-types">Windows Firewall with Advanced Security Enumerated Types</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference">Windows Firewall with Advanced Security Reference</a>
 

 

