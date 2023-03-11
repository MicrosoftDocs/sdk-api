---
UID: NE:icftypes.NET_FW_POLICY_TYPE_
title: NET_FW_POLICY_TYPE (icftypes.h)
description: The NET_FW_POLICY_TYPE enumerated type specifies the type of policy.
helpviewer_keywords: ["NET_FW_POLICY_EFFECTIVE","NET_FW_POLICY_GROUP","NET_FW_POLICY_LOCAL","NET_FW_POLICY_TYPE","NET_FW_POLICY_TYPE enumeration [ICS/ICF]","NET_FW_POLICY_TYPE_MAX","icftypes/NET_FW_POLICY_EFFECTIVE","icftypes/NET_FW_POLICY_GROUP","icftypes/NET_FW_POLICY_LOCAL","icftypes/NET_FW_POLICY_TYPE","icftypes/NET_FW_POLICY_TYPE_MAX","ics.net_fw_policy_type"]
old-location: ics\net_fw_policy_type.htm
tech.root: ics
ms.assetid: 10b052d6-55d1-4583-9fd4-ebb02548d1db
ms.date: 12/05/2018
ms.keywords: NET_FW_POLICY_EFFECTIVE, NET_FW_POLICY_GROUP, NET_FW_POLICY_LOCAL, NET_FW_POLICY_TYPE, NET_FW_POLICY_TYPE enumeration [ICS/ICF], NET_FW_POLICY_TYPE_MAX, icftypes/NET_FW_POLICY_EFFECTIVE, icftypes/NET_FW_POLICY_GROUP, icftypes/NET_FW_POLICY_LOCAL, icftypes/NET_FW_POLICY_TYPE, icftypes/NET_FW_POLICY_TYPE_MAX, ics.net_fw_policy_type
req.header: icftypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
targetos: Windows
req.typenames: NET_FW_POLICY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_POLICY_TYPE_
 - icftypes/NET_FW_POLICY_TYPE_
 - NET_FW_POLICY_TYPE
 - icftypes/NET_FW_POLICY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Icftypes.h
api_name:
 - NET_FW_POLICY_TYPE
---

# NET_FW_POLICY_TYPE enumeration


## -description

> [!NOTE]
>The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the [Firewall with Advanced Security](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)Windows API is recommended.

The **NET_FW_POLICY_TYPE** enumerated type specifies the type of policy.

## -enum-fields

### -field NET_FW_POLICY_GROUP:0

Policy type is group.

### -field NET_FW_POLICY_LOCAL

Policy type is local.

### -field NET_FW_POLICY_EFFECTIVE

Policy type is effective.

### -field NET_FW_POLICY_TYPE_MAX

Used for boundary checking only. Not valid for application programming.

## -see-also

[Windows Firewall Enumerated Types](/previous-versions/windows/desktop/ics/windows-firewall-enumerated-types)

[Windows Firewall Reference](/previous-versions/windows/desktop/ics/windows-firewall-reference)
