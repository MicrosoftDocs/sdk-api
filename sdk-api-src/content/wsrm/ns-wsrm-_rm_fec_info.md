---
UID: NS:wsrm._RM_FEC_INFO
title: "_RM_FEC_INFO"
author: windows-sdk-content
description: The RM_FEC_INFO structure specifies settings for using forward error correction (FEC) with Reliable Multicast. This structure is used with the RM_USE_FEC socket option.
old-location: winsock\rm_fec_info.htm
old-project: winsock
ms.assetid: c5dcf0fd-dffc-473b-a8f2-0abbaa0ec446
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: RM_FEC_INFO, RM_FEC_INFO structure [Winsock], _RM_FEC_INFO, winsock.rm_fec_info, wsrm/RM_FEC_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsrm.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RM_FEC_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsrm.h
api_name:
 - RM_FEC_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _RM_FEC_INFO structure


## -description


The <b>RM_FEC_INFO</b> structure specifies settings for using forward error correction (FEC) with Reliable Multicast. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/ms740525(v=VS.85).aspx">RM_USE_FEC</a> socket option.


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



The <a href="https://msdn.microsoft.com/en-us/library/ms740525(v=VS.85).aspx">RM_USE_FEC</a> socket option notifies the Reliable Multicast sender to apply forward error correction techniques to send repair data. there are three modes of using forward error correction:

<ol>
<li>Pro-active parity packets only</li>
<li>OnDemand parity packets only</li>
<li>Both pro-active and OnDemand parity packets</li>
</ol>
Since the use of this structure implies the need for forward error correction, either the <b>FECProActivePackets</b> or <b>fFECOnDemandParityEnabled</b> member must be nonzero, otherwise the function call fails.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms740525(v=VS.85).aspx">RM_USE_FEC</a>



<a href="https://msdn.microsoft.com/81c203ed-739f-4a06-99a1-9a99c6164edc">Reliable Multicast Programming</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket
  Options</a>
 

 

