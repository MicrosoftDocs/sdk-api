---
UID: NS:spb.SPB_TRANSFER_LIST_ENTRY
title: SPB_TRANSFER_LIST_ENTRY
author: windows-driver-content
description: The SPB_TRANSFER_LIST_ENTRY structure describes a single transfer in an I/O transfer sequence.
old-location: spb\spb_transfer_list_entry.htm
old-project: SPB
ms.assetid: e13b7a7e-4acb-4a77-ac46-94af2ebccc20
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSPB_TRANSFER_LIST_ENTRY, PSPB_TRANSFER_LIST_ENTRY, PSPB_TRANSFER_LIST_ENTRY structure pointer [Buses], SPB.spb_transfer_list_entry, SPB_TRANSFER_LIST_ENTRY, SPB_TRANSFER_LIST_ENTRY structure [Buses], spb/PSPB_TRANSFER_LIST_ENTRY, spb/SPB_TRANSFER_LIST_ENTRY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: spb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 8.
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
req.typenames: SPB_TRANSFER_LIST_ENTRY, *PSPB_TRANSFER_LIST_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Spb.h
api_name:
-	SPB_TRANSFER_LIST_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SPB_TRANSFER_LIST_ENTRY structure


## -description


The <b>SPB_TRANSFER_LIST_ENTRY</b> structure describes a single transfer in an <a href="https://msdn.microsoft.com/7415DB28-5E93-4F47-B169-7C652969D4C7">I/O transfer sequence</a>.


## -struct-fields




### -field Direction

The direction of the transfer.  This member is set to one of the following <a href="https://msdn.microsoft.com/library/windows/hardware/hh406220">SPB_TRANSFER_DIRECTION</a> enumeration values:

<ul>
<li><b>SpbTransferDirectionFromDevice</b></li>
<li><b>SpbTransferDirectionToDevice</b></li>
</ul>

### -field DelayInUs

An optional delay, in microseconds, before this transfer begins. For more information, see the description of the <b>DelayInUs</b> member in <a href="https://msdn.microsoft.com/library/windows/hardware/hh406218">SPB_TRANSFER_DESCRIPTOR</a>.


### -field Buffer

The buffer for this transfer. This member uses one of the following buffer formats: simple buffer, scatter-gather list, or (for kernel-mode clients) MDL. For more information about buffer formats, see <a href="https://msdn.microsoft.com/library/windows/hardware/hh406215">SPB_TRANSFER_BUFFER</a>.


## -remarks



To request an I/O transfer sequence for a target device on the bus, a client (peripheral driver) of the SPB controller driver sends an <a href="https://msdn.microsoft.com/library/windows/hardware/hh450857">IOCTL_SPB_EXECUTE_SEQUENCE</a> request that describes the sequence. The transfers in the sequence are described by an <a href="https://msdn.microsoft.com/library/windows/hardware/hh406221">SPB_TRANSFER_LIST</a> structure that is followed by an array of one or more <b>SPB_TRANSFER_LIST_ENTRY</b> structures. Each element in this array describes an individual transfer in the sequence.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450857">IOCTL_SPB_EXECUTE_SEQUENCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406215">SPB_TRANSFER_BUFFER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406218">SPB_TRANSFER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406220">SPB_TRANSFER_DIRECTION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406221">SPB_TRANSFER_LIST</a>
 

 

