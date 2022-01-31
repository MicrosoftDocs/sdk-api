---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0011
title: WDSTRANSPORT_UDP_PORT_POLICY (wdstptmgmt.h)
description: Specifies which policy WDS transport services should use when allocating UDP ports.
helpviewer_keywords: ["*PWDSTRANSPORT_UDP_PORT_POLICY","WDSTRANSPORT_UDP_PORT_POLICY","WDSTRANSPORT_UDP_PORT_POLICY enumeration [Windows Deployment Services]","WDSTRANSPORT_UDP_PORT_POLICY","*PWDSTRANSPORT_UDP_PORT_POLICY","WDSTRANSPORT_UDP_PORT_POLICY","*PWDSTRANSPORT_UDP_PORT_POLICY enumeration [Windows Deployment Services]","WdsTptUdpPortPolicyDynamic","WdsTptUdpPortPolicyFixed","wds.wdstransport_udp_port_policy","wdstptmgmt/WDSTRANSPORT_UDP_PORT_POLICY","wdstptmgmt/WdsTptUdpPortPolicyDynamic","wdstptmgmt/WdsTptUdpPortPolicyFixed"]
old-location: wds\wdstransport_udp_port_policy.htm
tech.root: wds
ms.assetid: A2049125-B40A-44F0-83AF-C3F5B983ABAE
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_UDP_PORT_POLICY, WDSTRANSPORT_UDP_PORT_POLICY, WDSTRANSPORT_UDP_PORT_POLICY enumeration [Windows Deployment Services], WDSTRANSPORT_UDP_PORT_POLICY,*PWDSTRANSPORT_UDP_PORT_POLICY, WDSTRANSPORT_UDP_PORT_POLICY,*PWDSTRANSPORT_UDP_PORT_POLICY enumeration [Windows Deployment Services], WdsTptUdpPortPolicyDynamic, WdsTptUdpPortPolicyFixed, wds.wdstransport_udp_port_policy, wdstptmgmt/WDSTRANSPORT_UDP_PORT_POLICY, wdstptmgmt/WdsTptUdpPortPolicyDynamic, wdstptmgmt/WdsTptUdpPortPolicyFixed'
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WDSTRANSPORT_UDP_PORT_POLICY, *PWDSTRANSPORT_UDP_PORT_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0011
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0011
 - PWDSTRANSPORT_UDP_PORT_POLICY
 - wdstptmgmt/PWDSTRANSPORT_UDP_PORT_POLICY
 - WDSTRANSPORT_UDP_PORT_POLICY
 - wdstptmgmt/WDSTRANSPORT_UDP_PORT_POLICY
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
 - WDSTRANSPORT_UDP_PORT_POLICY, *PWDSTRANSPORT_UDP_PORT_POLICY
---

# WDSTRANSPORT_UDP_PORT_POLICY enumeration


## -description

Specifies which policy WDS transport services should use when allocating UDP ports.

## -enum-fields

### -field WdsTptUdpPortPolicyDynamic:0

Use Windows Sockets (Winsock) to get a dynamic UDP port.

### -field WdsTptUdpPortPolicyFixed:1

Assign a fixed UDP port from a specified range of UDP ports.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportservicepolicy2-get_udpportpolicy">IWdsTransportServicePolicy2::UdpPortPolicy Property</a>
