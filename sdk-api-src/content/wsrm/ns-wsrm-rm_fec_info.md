---
UID: NS:wsrm._RM_FEC_INFO
title: RM_FEC_INFO (wsrm.h)
description: The RM_FEC_INFO structure specifies settings for using forward error correction (FEC) with Reliable Multicast. This structure is used with the RM_USE_FEC socket option.
helpviewer_keywords: ["RM_FEC_INFO","RM_FEC_INFO structure [Winsock]","winsock.rm_fec_info","wsrm/RM_FEC_INFO"]
old-location: winsock\rm_fec_info.htm
tech.root: WinSock
ms.assetid: c5dcf0fd-dffc-473b-a8f2-0abbaa0ec446
ms.date: 12/05/2018
ms.keywords: RM_FEC_INFO, RM_FEC_INFO structure [Winsock], winsock.rm_fec_info, wsrm/RM_FEC_INFO
req.header: wsrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: RM_FEC_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_FEC_INFO
 - wsrm/_RM_FEC_INFO
 - RM_FEC_INFO
 - wsrm/RM_FEC_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsrm.h
api_name:
 - RM_FEC_INFO
---

# RM_FEC_INFO structure


## -description

The <b>RM_FEC_INFO</b> structure specifies settings for using forward error correction (FEC) with Reliable Multicast. This structure is used with the <a href="/windows/desktop/WinSock/socket-options">RM_USE_FEC</a> socket option.

## -struct-fields

### -field FECBlockSize

Maximum number of packets that can be sent for any group, including original data and parity packets. Maximum and default value is 255.

### -field FECProActivePackets

Number of packets to send proactively with each group. Use this option when the network is dispersed, and upstream NAK requests would have an impact on throughput.

### -field FECGroupSize

Number of packets to be treated as one group for the purpose of computing parity packets. Group size must be a power of two. In lossy networks, keep the group size relatively small.

### -field fFECOnDemandParityEnabled

Specifies whether the sender is enabled for sending parity repair packets. When <b>TRUE</b>, receivers should only request parity repair packets.

## -remarks

The <a href="/windows/desktop/WinSock/socket-options">RM_USE_FEC</a> socket option notifies the Reliable Multicast sender to apply forward error correction techniques to send repair data. there are three modes of using forward error correction:

<ol>
<li>Pro-active parity packets only</li>
<li>OnDemand parity packets only</li>
<li>Both pro-active and OnDemand parity packets</li>
</ol>
Since the use of this structure implies the need for forward error correction, either the <b>FECProActivePackets</b> or <b>fFECOnDemandParityEnabled</b> member must be nonzero, otherwise the function call fails.

## -see-also

<a href="/windows/desktop/WinSock/socket-options">RM_USE_FEC</a>



<a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">Reliable Multicast Programming</a>



<a href="/windows/desktop/WinSock/socket-options">Socket
  Options</a>