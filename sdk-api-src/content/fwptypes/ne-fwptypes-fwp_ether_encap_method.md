---
UID: NE:fwptypes.FWP_ETHER_ENCAP_METHOD_
title: FWP_ETHER_ENCAP_METHOD (fwptypes.h)
description: Specifies the method of encapsulating Ethernet II and SNAP traffic. Reserved.
helpviewer_keywords: ["FWP_ETHER_ENCAP_METHOD","FWP_ETHER_ENCAP_METHOD enumeration [Filtering]","FWP_ETHER_ENCAP_METHOD_ETHER_V2","FWP_ETHER_ENCAP_METHOD_SNAP","FWP_ETHER_ENCAP_METHOD_SNAP_W_OUI_ZERO","fwp.fwp_ether_encap_method","fwptypes/FWP_ETHER_ENCAP_METHOD","fwptypes/FWP_ETHER_ENCAP_METHOD_ETHER_V2","fwptypes/FWP_ETHER_ENCAP_METHOD_SNAP","fwptypes/FWP_ETHER_ENCAP_METHOD_SNAP_W_OUI_ZERO"]
old-location: fwp\fwp_ether_encap_method.htm
tech.root: fwp
ms.assetid: fd94a02e-ba2d-4f99-a340-11f2e594f319
ms.date: 12/05/2018
ms.keywords: FWP_ETHER_ENCAP_METHOD, FWP_ETHER_ENCAP_METHOD enumeration [Filtering], FWP_ETHER_ENCAP_METHOD_ETHER_V2, FWP_ETHER_ENCAP_METHOD_SNAP, FWP_ETHER_ENCAP_METHOD_SNAP_W_OUI_ZERO, fwp.fwp_ether_encap_method, fwptypes/FWP_ETHER_ENCAP_METHOD, fwptypes/FWP_ETHER_ENCAP_METHOD_ETHER_V2, fwptypes/FWP_ETHER_ENCAP_METHOD_SNAP, fwptypes/FWP_ETHER_ENCAP_METHOD_SNAP_W_OUI_ZERO
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWP_ETHER_ENCAP_METHOD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_ETHER_ENCAP_METHOD_
 - fwptypes/FWP_ETHER_ENCAP_METHOD_
 - FWP_ETHER_ENCAP_METHOD
 - fwptypes/FWP_ETHER_ENCAP_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_ETHER_ENCAP_METHOD
---

# FWP_ETHER_ENCAP_METHOD enumeration


## -description

The <b>FWP_ETHER_ENCAP_METHOD</b> enumerated type specifies the method of encapsulating Ethernet II and SNAP traffic. Reserved.

## -enum-fields

### -field FWP_ETHER_ENCAP_METHOD_ETHER_V2:0

Specifies Ethernet V2 encapsulation.

### -field FWP_ETHER_ENCAP_METHOD_SNAP:1

Specifies Subnet Access Protocol (SNAP) encapsulation with an unknown Organizationally Unique Identifier (OUI) and Service Access Point (SAP) prefix.

### -field FWP_ETHER_ENCAP_METHOD_SNAP_W_OUI_ZERO:3

Specifies SNAP encapsulation with a recognized OUI and a SAP prefix of 03.AA.AA.00.00.00 + Ethertype.

## -remarks

This enumeration is reserved.

