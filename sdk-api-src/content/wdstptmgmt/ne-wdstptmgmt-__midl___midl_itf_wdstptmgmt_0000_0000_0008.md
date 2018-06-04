---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

