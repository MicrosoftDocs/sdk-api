---
UID: NE:icftypes.NET_FW_IP_VERSION_
title: NET_FW_IP_VERSION (icftypes.h)
description: Specifies the IP version for a port.
helpviewer_keywords: ["NET_FW_IP_VERSION","NET_FW_IP_VERSION enumeration [ICS/ICF]","NET_FW_IP_VERSION_ANY","NET_FW_IP_VERSION_MAX","NET_FW_IP_VERSION_V4","NET_FW_IP_VERSION_V6","icftypes/NET_FW_IP_VERSION","icftypes/NET_FW_IP_VERSION_ANY","icftypes/NET_FW_IP_VERSION_MAX","icftypes/NET_FW_IP_VERSION_V4","icftypes/NET_FW_IP_VERSION_V6","ics.net_fw_ip_version"]
old-location: ics\net_fw_ip_version.htm
tech.root: ics
ms.assetid: f322c914-e84f-4c13-8200-06e5fe2bdab7
ms.date: 12/05/2018
ms.keywords: NET_FW_IP_VERSION, NET_FW_IP_VERSION enumeration [ICS/ICF], NET_FW_IP_VERSION_ANY, NET_FW_IP_VERSION_MAX, NET_FW_IP_VERSION_V4, NET_FW_IP_VERSION_V6, icftypes/NET_FW_IP_VERSION, icftypes/NET_FW_IP_VERSION_ANY, icftypes/NET_FW_IP_VERSION_MAX, icftypes/NET_FW_IP_VERSION_V4, icftypes/NET_FW_IP_VERSION_V6, ics.net_fw_ip_version
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
req.typenames: NET_FW_IP_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_IP_VERSION_
 - icftypes/NET_FW_IP_VERSION_
 - NET_FW_IP_VERSION
 - icftypes/NET_FW_IP_VERSION
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
 - NET_FW_IP_VERSION
---

# NET_FW_IP_VERSION enumeration


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The 
<b>NET_FW_IP_VERSION</b> enumerated type specifies the IP version for a port.

## -enum-fields

### -field NET_FW_IP_VERSION_V4:0

The port supports IPv4.

### -field NET_FW_IP_VERSION_V6

The port supports IPv6.

### -field NET_FW_IP_VERSION_ANY

The port supports either version of IP.

### -field NET_FW_IP_VERSION_MAX

This value is used for boundary checking only and is not valid for application programming.

## -see-also

<a href="/previous-versions/windows/desktop/ics/windows-firewall-enumerated-types">Windows Firewall Enumerated Types</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-reference">Windows Firewall Reference</a>
