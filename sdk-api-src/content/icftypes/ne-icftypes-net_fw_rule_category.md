---
UID: NE:icftypes.NET_FW_RULE_CATEGORY_
title: NET_FW_RULE_CATEGORY (icftypes.h)
description: The firewall rule category.
helpviewer_keywords: ["NET_FW_RULE_CATEGORY","NET_FW_RULE_CATEGORY enumeration [ICS/ICF]","NET_FW_RULE_CATEGORY_BOOT","NET_FW_RULE_CATEGORY_CONSEC","NET_FW_RULE_CATEGORY_FIREWALL","NET_FW_RULE_CATEGORY_MAX","NET_FW_RULE_CATEGORY_STEALTH","icftypes/NET_FW_RULE_CATEGORY","icftypes/NET_FW_RULE_CATEGORY_BOOT","icftypes/NET_FW_RULE_CATEGORY_CONSEC","icftypes/NET_FW_RULE_CATEGORY_FIREWALL","icftypes/NET_FW_RULE_CATEGORY_MAX","icftypes/NET_FW_RULE_CATEGORY_STEALTH","ics.net_fw_rule_category"]
old-location: ics\net_fw_rule_category.htm
tech.root: ics
ms.assetid: 87dcdd8a-a7c5-4a0c-8b05-716262b82f96
ms.date: 12/05/2018
ms.keywords: NET_FW_RULE_CATEGORY, NET_FW_RULE_CATEGORY enumeration [ICS/ICF], NET_FW_RULE_CATEGORY_BOOT, NET_FW_RULE_CATEGORY_CONSEC, NET_FW_RULE_CATEGORY_FIREWALL, NET_FW_RULE_CATEGORY_MAX, NET_FW_RULE_CATEGORY_STEALTH, icftypes/NET_FW_RULE_CATEGORY, icftypes/NET_FW_RULE_CATEGORY_BOOT, icftypes/NET_FW_RULE_CATEGORY_CONSEC, icftypes/NET_FW_RULE_CATEGORY_FIREWALL, icftypes/NET_FW_RULE_CATEGORY_MAX, icftypes/NET_FW_RULE_CATEGORY_STEALTH, ics.net_fw_rule_category
req.header: icftypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: NET_FW_RULE_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_RULE_CATEGORY_
 - icftypes/NET_FW_RULE_CATEGORY_
 - NET_FW_RULE_CATEGORY
 - icftypes/NET_FW_RULE_CATEGORY
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
 - NET_FW_RULE_CATEGORY
---

# NET_FW_RULE_CATEGORY enumeration


## -description

The <b>NET_FW_RULE_CATEGORY</b> enumerated type specifies the firewall rule category.

## -enum-fields

### -field NET_FW_RULE_CATEGORY_BOOT:0

Specifies boot time filters.

### -field NET_FW_RULE_CATEGORY_STEALTH

Specifies stealth filters.

### -field NET_FW_RULE_CATEGORY_FIREWALL

Specifies firewall filters.

### -field NET_FW_RULE_CATEGORY_CONSEC

Specifies connection security filters.

### -field NET_FW_RULE_CATEGORY_MAX

Maximum value for testing purposes.

## -remarks

For more information about using <b>NET_FW_RULE_CATEGORY</b>, download the <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=08d23da9-ff0e-4e6f-b742-878ca1977c55">Windows Firewall and User Facing Impact</a> document.

## -see-also

<a href="/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-enumerated-types">Windows Firewall with Advanced Security Enumerated Types</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference">Windows Firewall with Advanced Security Reference</a>
