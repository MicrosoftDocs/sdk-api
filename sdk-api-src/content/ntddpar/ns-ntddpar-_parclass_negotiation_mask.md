---
UID: NS:ntddpar._PARCLASS_NEGOTIATION_MASK
title: "_PARCLASS_NEGOTIATION_MASK"
author: windows-driver-content
description: The PARCLASS_NEGOTIATION_MASK structure specifies the read and write protocols that a driver selects for a parallel device.
old-location: parports\parclass_negotiation_mask.htm
old-project: parports
ms.assetid: 6d246ec3-47f1-46da-8ac4-f073f91c0d44
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PPARCLASS_NEGOTIATION_MASK, PARCLASS_NEGOTIATION_MASK, PARCLASS_NEGOTIATION_MASK structure [Parallel Ports], PPARCLASS_NEGOTIATION_MASK, PPARCLASS_NEGOTIATION_MASK structure pointer [Parallel Ports], _PARCLASS_NEGOTIATION_MASK, cisspd_8afca893-6736-49a8-a2bd-efb3d97bb63d.xml, ntddpar/PARCLASS_NEGOTIATION_MASK, ntddpar/PPARCLASS_NEGOTIATION_MASK, parports.parclass_negotiation_mask"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddpar.h
req.include-header: Ntddpar.h
req.target-type: Windows
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
req.typenames: PARCLASS_NEGOTIATION_MASK, *PPARCLASS_NEGOTIATION_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddpar.h
api_name:
-	PARCLASS_NEGOTIATION_MASK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _PARCLASS_NEGOTIATION_MASK structure


## -description


The PARCLASS_NEGOTIATION_MASK structure specifies the read and write protocols that a driver selects for a parallel device.


## -struct-fields




### -field usReadMask

Specifies the read protocols. For read and write protocol values, see the constants that are defined in <i>ntddpar.h</i> (from NONE to ECP_ANY).


### -field usWriteMask

Specifies the write protocols.


## -remarks



A client specifies a set of requested protocols by setting a bitwise OR of the constants that represent each protocol. The system-supplied bus driver for parallel ports selects the fastest protocol that it supports from among those specified by the client. 

For more information, see <a href="https://msdn.microsoft.com/2ff53ed0-dbb7-4c8f-b6e4-5f7d20124a7c">Setting and Clearing a Communication Mode for a Parallel Device</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543975">IOCTL_IEEE1284_GET_MODE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543978">IOCTL_IEEE1284_NEGOTIATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544061">IOCTL_PAR_GET_DEFAULT_MODES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544365">PDETERMINE_IEEE_MODES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544386">PNEGOTIATE_IEEE_MODE</a>
 

 

