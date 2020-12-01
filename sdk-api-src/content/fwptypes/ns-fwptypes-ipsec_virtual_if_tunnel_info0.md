---
UID: NS:fwptypes.IPSEC_VIRTUAL_IF_TUNNEL_INFO0_
title: IPSEC_VIRTUAL_IF_TUNNEL_INFO0 (fwptypes.h)
description: Is used to store information specific to virtual interface tunneling.
helpviewer_keywords: ["IPSEC_VIRTUAL_IF_TUNNEL_INFO0","IPSEC_VIRTUAL_IF_TUNNEL_INFO0 structure [Filtering]","IPSEC_VIRTUAL_IF_TUNNEL_INFO0_","fwp.ipsec_virtual_if_tunnel_info0","fwptypes/IPSEC_VIRTUAL_IF_TUNNEL_INFO0"]
old-location: fwp\ipsec_virtual_if_tunnel_info0.htm
tech.root: fwp
ms.assetid: 91af0790-865f-44f5-b6c8-fd048bf99125
ms.date: 12/05/2018
ms.keywords: IPSEC_VIRTUAL_IF_TUNNEL_INFO0, IPSEC_VIRTUAL_IF_TUNNEL_INFO0 structure [Filtering], IPSEC_VIRTUAL_IF_TUNNEL_INFO0_, fwp.ipsec_virtual_if_tunnel_info0, fwptypes/IPSEC_VIRTUAL_IF_TUNNEL_INFO0
req.header: fwptypes.h
req.include-header: Ipsectypes.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_VIRTUAL_IF_TUNNEL_INFO0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_VIRTUAL_IF_TUNNEL_INFO0_
 - fwptypes/IPSEC_VIRTUAL_IF_TUNNEL_INFO0_
 - IPSEC_VIRTUAL_IF_TUNNEL_INFO0
 - fwptypes/IPSEC_VIRTUAL_IF_TUNNEL_INFO0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - IPSEC_VIRTUAL_IF_TUNNEL_INFO0
---

# IPSEC_VIRTUAL_IF_TUNNEL_INFO0 structure


## -description

The <b>IPSEC_VIRTUAL_IF_TUNNEL_INFO0</b> structure is used to store information specific to virtual interface tunneling.

## -struct-fields

### -field virtualIfTunnelId

ID of the  virtual interface tunnel state.

### -field trafficSelectorId

ID of the virtual interface tunneling traffic selector(s).

## -remarks

 The <b>IPSEC_VIRTUAL_IF_TUNNEL_INFO0</b> structure is applicable only to Internet Key Exchange version 2 (IKEv2).

<b>IPSEC_VIRTUAL_IF_TUNNEL_INFO0</b> is a specific implementation of IPSEC_VIRTUAL_IF_TUNNEL_INFO. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>