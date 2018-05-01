---
UID: NS:spb.SPB_TRANSFER_BUFFER_LIST_ENTRY
title: SPB_TRANSFER_BUFFER_LIST_ENTRY
author: windows-driver-content
description: The SPB_TRANSFER_BUFFER_LIST_ENTRY structure describes either a simple transfer buffer, or an element in an array of one or more transfer buffers.
old-location: spb\spb_transfer_buffer_list_entry.htm
old-project: SPB
ms.assetid: C53F4F44-5338-4BEF-8055-AE4AC37002AC
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSPB_TRANSFER_BUFFER_LIST_ENTRY, PSPB_TRANSFER_BUFFER_LIST_ENTRY, PSPB_TRANSFER_BUFFER_LIST_ENTRY structure pointer [Buses], SPB.spb_transfer_buffer_list_entry, SPB_TRANSFER_BUFFER_LIST_ENTRY, SPB_TRANSFER_BUFFER_LIST_ENTRY structure [Buses], spb/PSPB_TRANSFER_BUFFER_LIST_ENTRY, spb/SPB_TRANSFER_BUFFER_LIST_ENTRY"
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
req.typenames: SPB_TRANSFER_BUFFER_LIST_ENTRY, *PSPB_TRANSFER_BUFFER_LIST_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Spb.h
api_name:
-	SPB_TRANSFER_BUFFER_LIST_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SPB_TRANSFER_BUFFER_LIST_ENTRY structure


## -description


The <b>SPB_TRANSFER_BUFFER_LIST_ENTRY</b> structure describes either a simple transfer buffer, or an element in an array of one or more transfer buffers.


## -struct-fields




### -field Buffer

The virtual address of the transfer buffer. For a transfer that is requested by a client of the SPB controller driver that runs in user mode, this buffer must reside entirely in user-mode memory.


### -field BufferCb

The size, in bytes, of the transfer buffer that <b>Buffer</b> points to.


## -remarks



To request an <a href="https://msdn.microsoft.com/7415DB28-5E93-4F47-B169-7C652969D4C7">I/O transfer sequence</a> for a target device on the bus, a client (peripheral driver) of the SPB controller driver sends an <a href="https://msdn.microsoft.com/library/windows/hardware/hh450857">IOCTL_SPB_EXECUTE_SEQUENCE</a> request that describes the sequence. The transfers in the sequence are described by an <a href="https://msdn.microsoft.com/library/windows/hardware/hh406221">SPB_TRANSFER_LIST</a> structure that is followed by an array of one or more <a href="https://msdn.microsoft.com/library/windows/hardware/hh406223">SPB_TRANSFER_LIST_ENTRY</a> structures. Each element in this array describes an individual transfer in the sequence, and each element contains an <a href="https://msdn.microsoft.com/library/windows/hardware/hh406215">SPB_TRANSFER_BUFFER</a> structure that describes the buffer to use for the transfer.

If the buffer format is  <b>SpbTransferBufferFormatSimple</b>, an  <b>SPB_TRANSFER_BUFFER</b> structure contains a single <b>SPB_TRANSFER_BUFFER_LIST_ENTRY</b> structure that describes a simple buffer that is specified by an address and a length. If the buffer format is <b>SpbTransferBufferFormatList</b>, the buffer is a scatter-gather list, and the  <b>SPB_TRANSFER_BUFFER</b> structure contains a pointer to an <b>SPB_TRANSFER_BUFFER_LIST_ENTRY</b> array that describes the list.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450857">IOCTL_SPB_EXECUTE_SEQUENCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406215">SPB_TRANSFER_BUFFER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406221">SPB_TRANSFER_LIST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406223">SPB_TRANSFER_LIST_ENTRY</a>
 

 

