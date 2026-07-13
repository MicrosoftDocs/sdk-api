---
UID: NE:icftypes.NET_FW_SCOPE_
title: NET_FW_SCOPE (icftypes.h)
description: Specifies the scope of addresses from which a port can listen.
helpviewer_keywords: ["NET_FW_SCOPE","NET_FW_SCOPE enumeration [ICS/ICF]","NET_FW_SCOPE_ALL","NET_FW_SCOPE_CUSTOM","NET_FW_SCOPE_LOCAL_SUBNET","NET_FW_SCOPE_MAX","icftypes/NET_FW_SCOPE","icftypes/NET_FW_SCOPE_ALL","icftypes/NET_FW_SCOPE_CUSTOM","icftypes/NET_FW_SCOPE_LOCAL_SUBNET","icftypes/NET_FW_SCOPE_MAX","ics.net_fw_scope"]
old-location: ics\net_fw_scope.htm
tech.root: ics
ms.assetid: 71f52d88-efd3-4037-86bc-7ec1cfa9642f
ms.date: 12/05/2018
ms.keywords: NET_FW_SCOPE, NET_FW_SCOPE enumeration [ICS/ICF], NET_FW_SCOPE_ALL, NET_FW_SCOPE_CUSTOM, NET_FW_SCOPE_LOCAL_SUBNET, NET_FW_SCOPE_MAX, icftypes/NET_FW_SCOPE, icftypes/NET_FW_SCOPE_ALL, icftypes/NET_FW_SCOPE_CUSTOM, icftypes/NET_FW_SCOPE_LOCAL_SUBNET, icftypes/NET_FW_SCOPE_MAX, ics.net_fw_scope
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
req.typenames: NET_FW_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_SCOPE_
 - icftypes/NET_FW_SCOPE_
 - NET_FW_SCOPE
 - icftypes/NET_FW_SCOPE
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
 - NET_FW_SCOPE
---

# NET_FW_SCOPE enumeration


## -description

> [!NOTE]
>The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the [Firewall with Advanced Security](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)Windows API is recommended.

The 
<b>NET_FW_SCOPE</b> enumerated type  specifies the scope of addresses from which a port can listen.

## -enum-fields

### -field NET_FW_SCOPE_ALL:0

Scope is all.

### -field NET_FW_SCOPE_LOCAL_SUBNET

Scope is local subnet only.

### -field NET_FW_SCOPE_CUSTOM

Scope is custom.

### -field NET_FW_SCOPE_MAX

Used for boundary checking only. Not valid for application programming.

## -see-also

[Windows Firewall Enumerated Types](/previous-versions/windows/desktop/ics/windows-firewall-enumerated-types)

[Windows Firewall Reference](/previous-versions/windows/desktop/ics/windows-firewall-reference)
