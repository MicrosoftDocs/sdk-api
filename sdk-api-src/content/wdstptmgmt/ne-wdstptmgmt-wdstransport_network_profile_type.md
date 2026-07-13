---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0008
title: WDSTRANSPORT_NETWORK_PROFILE_TYPE (wdstptmgmt.h)
description: Defines settings that are used by WDS transport protocols to optimize data transfer on the network.
helpviewer_keywords: ["*PWDSTRANSPORT_NETWORK_PROFILE_TYPE","WDSTRANSPORT_NETWORK_PROFILE_TYPE","WDSTRANSPORT_NETWORK_PROFILE_TYPE enumeration [Windows Deployment Services]","WdsTptNetworkProfile100Mbps","WdsTptNetworkProfile10Mbps","WdsTptNetworkProfile1Gbps","WdsTptNetworkProfileCustom","WdsTptNetworkProfileUnknown","wds.wdstransport_network_profile_type","wdstptmgmt/WDSTRANSPORT_NETWORK_PROFILE_TYPE","wdstptmgmt/WdsTptNetworkProfile100Mbps","wdstptmgmt/WdsTptNetworkProfile10Mbps","wdstptmgmt/WdsTptNetworkProfile1Gbps","wdstptmgmt/WdsTptNetworkProfileCustom","wdstptmgmt/WdsTptNetworkProfileUnknown"]
old-location: wds\wdstransport_network_profile_type.htm
tech.root: wds
ms.assetid: 2fa0d8d8-5ced-402b-8452-bf2e2aa4b19f
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_NETWORK_PROFILE_TYPE, WDSTRANSPORT_NETWORK_PROFILE_TYPE, WDSTRANSPORT_NETWORK_PROFILE_TYPE enumeration [Windows Deployment Services], WdsTptNetworkProfile100Mbps, WdsTptNetworkProfile10Mbps, WdsTptNetworkProfile1Gbps, WdsTptNetworkProfileCustom, WdsTptNetworkProfileUnknown, wds.wdstransport_network_profile_type, wdstptmgmt/WDSTRANSPORT_NETWORK_PROFILE_TYPE, wdstptmgmt/WdsTptNetworkProfile100Mbps, wdstptmgmt/WdsTptNetworkProfile10Mbps, wdstptmgmt/WdsTptNetworkProfile1Gbps, wdstptmgmt/WdsTptNetworkProfileCustom, wdstptmgmt/WdsTptNetworkProfileUnknown'
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
req.typenames: WDSTRANSPORT_NETWORK_PROFILE_TYPE, *PWDSTRANSPORT_NETWORK_PROFILE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0008
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0008
 - PWDSTRANSPORT_NETWORK_PROFILE_TYPE
 - wdstptmgmt/PWDSTRANSPORT_NETWORK_PROFILE_TYPE
 - WDSTRANSPORT_NETWORK_PROFILE_TYPE
 - wdstptmgmt/WDSTRANSPORT_NETWORK_PROFILE_TYPE
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
 - WDSTRANSPORT_NETWORK_PROFILE_TYPE
---

# WDSTRANSPORT_NETWORK_PROFILE_TYPE enumeration


## -description

Defines  settings that are used by WDS transport protocols to optimize data transfer on the network. The network profile setting values are optimized for different network speeds and in most cases should not be changed. A custom  network profile is included to enable administrators to try different values and find what suits their network best.

## -enum-fields

### -field WdsTptNetworkProfileUnknown:0

Default value that indicates that the network profile is not known.

### -field WdsTptNetworkProfileCustom:1

Indicates that the server should use the custom network profile. This is a profile whose settings can be directly modified by administrators if they need to further customize their settings rather than use one of the fixed, inbox profiles. Note that settings for this profile start with values identical to those of the 100-Mbps profile.

### -field WdsTptNetworkProfile10Mbps:2

Indicates that the server should use the 10-Mbps network profile, which is optimized for slow 10-Mbps networks.

### -field WdsTptNetworkProfile100Mbps:3

Indicates that the server should use the 100-Mbps network profile, which is optimized for mainstream 100-Mbps networks. This is the default profile selected for use on a freshly installed WDS server.

### -field WdsTptNetworkProfile1Gbps:4

Indicates that the server should use the 1-Gbps network profile, which is optimized for fast 1-Gbps or higher networks, such as those used in high-end data centers.

