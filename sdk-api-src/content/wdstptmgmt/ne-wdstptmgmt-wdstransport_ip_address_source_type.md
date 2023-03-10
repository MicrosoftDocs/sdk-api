---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0007
title: WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE (wdstptmgmt.h)
description: Indicates the source from which the WDS multicast provider obtains a multicast address for a new session.
helpviewer_keywords: ["*PWDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE","WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE","WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE enumeration [Windows Deployment Services]","WdsTptIpAddressSourceDhcp","WdsTptIpAddressSourceRange","WdsTptIpAddressSourceUnknown","wds.wdstransport_ip_address_source_type","wdstptmgmt/WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE","wdstptmgmt/WdsTptIpAddressSourceDhcp","wdstptmgmt/WdsTptIpAddressSourceRange","wdstptmgmt/WdsTptIpAddressSourceUnknown"]
old-location: wds\wdstransport_ip_address_source_type.htm
tech.root: wds
ms.assetid: bc16cf5e-2cfe-480b-b67c-546b47ef2518
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE, WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE, WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE enumeration [Windows Deployment Services], WdsTptIpAddressSourceDhcp, WdsTptIpAddressSourceRange, WdsTptIpAddressSourceUnknown, wds.wdstransport_ip_address_source_type, wdstptmgmt/WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE, wdstptmgmt/WdsTptIpAddressSourceDhcp, wdstptmgmt/WdsTptIpAddressSourceRange, wdstptmgmt/WdsTptIpAddressSourceUnknown'
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
targetos: Windows
req.typenames: WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE, *PWDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0007
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0007
 - PWDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE
 - wdstptmgmt/PWDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE
 - WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE
 - wdstptmgmt/WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstptmgmt.h
api_name:
 - WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE
---

# WDSTRANSPORT_IP_ADDRESS_SOURCE_TYPE enumeration


## -description

Indicates the source from which the WDS multicast provider obtains a multicast address for a new session.

## -enum-fields

### -field WdsTptIpAddressSourceUnknown:0

Default value that indicates that the IP address source is not known.

### -field WdsTptIpAddressSourceDhcp:1

Indicates that the server should use the <a href="/previous-versions/windows/desktop/madcap/madcap-start-page">Multicast Address Dynamic Client Allocation Protocol</a> (MADCAP) to obtain a multicast IP address. MADCAP is a protocol that enables applications to obtain, renew, and release multicast addresses, and its functionality is often included in DHCP servers, such as the Microsoft DHCP Server role.

### -field WdsTptIpAddressSourceRange:2

Indicates that the server should automatically select an available address from a multicast address range manually configured by the administrator.
