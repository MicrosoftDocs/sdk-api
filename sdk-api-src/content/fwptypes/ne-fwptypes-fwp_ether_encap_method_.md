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

# FWP_ETHER_ENCAP_METHOD_ enumeration


## -description


The <b>FWP_ETHER_ENCAP_METHOD</b> enumerated type specifies the method of encapsulating Ethernet II and SNAP traffic. Reserved.


## -enum-fields




### -field FWP_ETHER_ENCAP_METHOD_ETHER_V2

Specifies Ethernet V2 encapsulation.


### -field FWP_ETHER_ENCAP_METHOD_SNAP

Specifies Subnet Access Protocol (SNAP) encapsulation with an unknown Organizationally Unique Identifier (OUI) and Service Access Point (SAP) prefix.


### -field FWP_ETHER_ENCAP_METHOD_SNAP_W_OUI_ZERO

Specifies SNAP encapsulation with a recognized OUI and a SAP prefix of 03.AA.AA.00.00.00 + Ethertype. 


## -remarks



This enumeration is reserved.



