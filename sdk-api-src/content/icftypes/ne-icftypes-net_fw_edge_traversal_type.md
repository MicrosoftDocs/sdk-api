---
UID: NE:icftypes.NET_FW_EDGE_TRAVERSAL_TYPE_
title: NET_FW_EDGE_TRAVERSAL_TYPE (icftypes.h)
description: The conditions under which edge traversal traffic is allowed.
helpviewer_keywords: ["NET_FW_EDGE_TRAVERSAL_TYPE","NET_FW_EDGE_TRAVERSAL_TYPE enumeration [ICS/ICF]","NET_FW_EDGE_TRAVERSAL_TYPE_ALLOW","NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP","NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER","NET_FW_EDGE_TRAVERSAL_TYPE_DENY","icftypes/NET_FW_EDGE_TRAVERSAL_TYPE","icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_ALLOW","icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP","icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER","icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_DENY","ics.net_fw_edge_traversal_type"]
old-location: ics\net_fw_edge_traversal_type.htm
tech.root: ics
ms.assetid: 69efe4d1-3614-4e6f-9bc1-4bacb9a7a8eb
ms.date: 12/05/2018
ms.keywords: NET_FW_EDGE_TRAVERSAL_TYPE, NET_FW_EDGE_TRAVERSAL_TYPE enumeration [ICS/ICF], NET_FW_EDGE_TRAVERSAL_TYPE_ALLOW, NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP, NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER, NET_FW_EDGE_TRAVERSAL_TYPE_DENY, icftypes/NET_FW_EDGE_TRAVERSAL_TYPE, icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_ALLOW, icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP, icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER, icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_DENY, ics.net_fw_edge_traversal_type
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
req.typenames: NET_FW_EDGE_TRAVERSAL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_EDGE_TRAVERSAL_TYPE_
 - icftypes/NET_FW_EDGE_TRAVERSAL_TYPE_
 - NET_FW_EDGE_TRAVERSAL_TYPE
 - icftypes/NET_FW_EDGE_TRAVERSAL_TYPE
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
 - NET_FW_EDGE_TRAVERSAL_TYPE
---

# NET_FW_EDGE_TRAVERSAL_TYPE enumeration


## -description

The <b>NET_FW_EDGE_TRAVERSAL_TYPE</b> enumerated type specifies  the conditions under which edge traversal traffic is allowed.

## -enum-fields

### -field NET_FW_EDGE_TRAVERSAL_TYPE_DENY:0

Edge traversal traffic is always blocked.

This is the same as setting the EdgeTraversal property using <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> to <b>VARIANT_FALSE</b>.

### -field NET_FW_EDGE_TRAVERSAL_TYPE_ALLOW

Edge traversal traffic is always allowed.

This is the same as setting the EdgeTraversal property using <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> to <b>VARIANT_TRUE</b>.

### -field NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP

Edge traversal traffic is allowed when the application sets the <a href="/windows/desktop/WinSock/ipv6-protection-level">IPV6_PROTECTION_LEVEL</a> socket option to <b>PROTECTION_LEVEL_UNRESTRICTED</b>. Otherwise, it is blocked.

### -field NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER

The user is prompted whether to allow edge traversal traffic when the application sets the IPV6_PROTECTION_LEVEL socket option to <b>PROTECTION_LEVEL_UNRESTRICTED</b>. If the user chooses to allow  edge traversal traffic, the rule is modified to defer to the application's settings.

If the application has not set the IPV6_PROTECTION_LEVEL socket option to <b>PROTECTION_LEVEL_UNRESTRICTED</b>, edge traversal traffic is blocked.

In order to use this option, the firewall rule must have both the application path and protocol scopes specified. This option cannot be used if port(s) are defined.

## -remarks

    In order for Windows Firewall to dynamically allow edge traversal traffic, the application must use the  <a href="/windows/desktop/WinSock/ipv6-protection-level">IPV6_PROTECTION_LEVEL</a> socket option on the listening socket
        and set it to <b>PROTECTION_LEVEL_UNRESTRICTED</b> only in the cases where edge traversal traffic should be allowed. The Windows Firewall rule added for the application must then set 
            its edge traversal option  to <b>NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP</b> or <b>NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>



<a href="/windows/desktop/WinSock/ipv6-protection-level">IPV6_PROTECTION_LEVEL</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-enumerated-types">Windows Firewall with Advanced Security Enumerated Types</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference">Windows Firewall with Advanced Security Reference</a>
