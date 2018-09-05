---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0008
title: "__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0008"
author: windows-sdk-content
description: Defines settings that are used by WDS transport protocols to optimize data transfer on the network.
old-location: wds\wdstransport_network_profile_type.htm
old-project: Wds
ms.assetid: 2fa0d8d8-5ced-402b-8452-bf2e2aa4b19f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PWDSTRANSPORT_NETWORK_PROFILE_TYPE, WDSTRANSPORT_NETWORK_PROFILE_TYPE, WDSTRANSPORT_NETWORK_PROFILE_TYPE enumeration [Windows Deployment Services], WdsTptNetworkProfile100Mbps, WdsTptNetworkProfile10Mbps, WdsTptNetworkProfile1Gbps, WdsTptNetworkProfileCustom, WdsTptNetworkProfileUnknown, __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0008, wds.wdstransport_network_profile_type, wdstptmgmt/WDSTRANSPORT_NETWORK_PROFILE_TYPE, wdstptmgmt/WdsTptNetworkProfile100Mbps, wdstptmgmt/WdsTptNetworkProfile10Mbps, wdstptmgmt/WdsTptNetworkProfile1Gbps, wdstptmgmt/WdsTptNetworkProfileCustom, wdstptmgmt/WdsTptNetworkProfileUnknown"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wdstptmgmt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WDSTRANSPORT_NETWORK_PROFILE_TYPE, *PWDSTRANSPORT_NETWORK_PROFILE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstptmgmt.h
api_name:
 - WDSTRANSPORT_NETWORK_PROFILE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0008 enumeration


## -description


Defines  settings that are used by WDS transport protocols to optimize data transfer on the network. The network profile setting values are optimized for different network speeds and in most cases should not be changed. A custom  network profile is included to enable administrators to try different values and find what suits their network best.


## -enum-fields




### -field WdsTptNetworkProfileUnknown

Default value that indicates that the network profile is not known.


### -field WdsTptNetworkProfileCustom

Indicates that the server should use the custom network profile. This is a profile whose settings can be directly modified by administrators if they need to further customize their settings rather than use one of the fixed, inbox profiles. Note that settings for this profile start with values identical to those of the 100-Mbps profile.


### -field WdsTptNetworkProfile10Mbps

Indicates that the server should use the 10-Mbps network profile, which is optimized for slow 10-Mbps networks.


### -field WdsTptNetworkProfile100Mbps

Indicates that the server should use the 100-Mbps network profile, which is optimized for mainstream 100-Mbps networks. This is the default profile selected for use on a freshly installed WDS server.


### -field WdsTptNetworkProfile1Gbps

Indicates that the server should use the 1-Gbps network profile, which is optimized for fast 1-Gbps or higher networks, such as those used in high-end data centers.

