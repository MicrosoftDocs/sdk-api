---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0011
title: "__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0011"
author: windows-driver-content
description: Specifies which policy WDS transport services should use when allocating UDP ports.
old-location: wds\wdstransport_udp_port_policy.htm
old-project: Wds
ms.assetid: A2049125-B40A-44F0-83AF-C3F5B983ABAE
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PWDSTRANSPORT_UDP_PORT_POLICY, WDSTRANSPORT_UDP_PORT_POLICY, WDSTRANSPORT_UDP_PORT_POLICY enumeration [Windows Deployment Services], WDSTRANSPORT_UDP_PORT_POLICY, *PWDSTRANSPORT_UDP_PORT_POLICY, WDSTRANSPORT_UDP_PORT_POLICY, *PWDSTRANSPORT_UDP_PORT_POLICY enumeration [Windows Deployment Services], WdsTptUdpPortPolicyDynamic, WdsTptUdpPortPolicyFixed, __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0011, wds.wdstransport_udp_port_policy, wdstptmgmt/WDSTRANSPORT_UDP_PORT_POLICY, wdstptmgmt/WdsTptUdpPortPolicyDynamic, wdstptmgmt/WdsTptUdpPortPolicyFixed"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: WDSTRANSPORT_UDP_PORT_POLICY, *PWDSTRANSPORT_UDP_PORT_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdstptmgmt.h
api_name:
-	WDSTRANSPORT_UDP_PORT_POLICY, *PWDSTRANSPORT_UDP_PORT_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0011 enumeration


## -description


Specifies which policy WDS transport services should use when allocating UDP ports.  


## -enum-fields




### -field WdsTptUdpPortPolicyDynamic

Use Windows Sockets (Winsock) to get a dynamic UDP port.


### -field WdsTptUdpPortPolicyFixed

Assign a fixed UDP port from a specified range of UDP ports.


## -see-also




<a href="https://msdn.microsoft.com/420400D4-98A4-497A-BEB3-54BD4057B0BE">IWdsTransportServicePolicy2::UdpPortPolicy Property</a>
 

 

