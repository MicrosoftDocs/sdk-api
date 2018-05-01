---
UID: NS:spb.SPB_TRANSFER_BUFFER
title: SPB_TRANSFER_BUFFER
author: windows-driver-content
description: The SPB_TRANSFER_BUFFER structure describes the data buffer for an individual transfer in an I/O transfer sequence.
old-location: spb\spb_transfer_buffer.htm
old-project: SPB
ms.assetid: E9C5B866-1EB0-4043-B22F-DF2F4CFAE64C
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSPB_TRANSFER_BUFFER, PSPB_TRANSFER_BUFFER, PSPB_TRANSFER_BUFFER structure pointer [Buses], SPB.spb_transfer_buffer, SPB_TRANSFER_BUFFER, SPB_TRANSFER_BUFFER structure [Buses], spb/PSPB_TRANSFER_BUFFER, spb/SPB_TRANSFER_BUFFER"
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
req.typenames: SPB_TRANSFER_BUFFER, *PSPB_TRANSFER_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Spb.h
api_name:
-	SPB_TRANSFER_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SPB_TRANSFER_BUFFER structure


## -description


The <b>SPB_TRANSFER_BUFFER</b> structure describes the data buffer for an individual transfer in an <a href="https://msdn.microsoft.com/7415DB28-5E93-4F47-B169-7C652969D4C7">I/O transfer sequence</a>.


## -struct-fields




### -field List

 


### -field ListCe

 


### -field Format

The buffer format.  This member is set to one of the following <a href="https://msdn.microsoft.com/library/windows/hardware/hh406216">SPB_TRANSFER_BUFFER_FORMAT</a> enumeration values:

<ul>
<li><b>SpbTransferBufferFormatSimple</b></li>
<li><b>SpbTransferBufferFormatList</b></li>
<li><b>SpbTransferBufferFormatSimpleNonPaged</b></li>
<li><b>SpbTransferBufferFormatMdl</b></li>
</ul>
<b>SpbTransferBufferFormatMdl</b> is a valid value only for I/O transfer sequences that are requested by clients of the SPB controller driver that are kernel-mode components.


#### - BufferList

A scatter-gather list that consists of an array of buffer descriptors. Use this member of the union if <b>Format</b> is <b>SpbTransferBufferFormatList</b>.



#### List

A pointer to an array of <b>SPB_TRANSFER_BUFFER_LIST_ENTRY</b> structures that describe the buffers in the scatter-gather list.



#### ListCe

The number of elements in the <b>List</b> array.


#### - Mdl

A pointer to an MDL that describes the buffer. This member is used only by kernel-mode clients. Use this member of the union if <b>Format</b> is <b>SpbTransferBufferFormatMdl</b>. For more information, see Remarks.


#### - Simple

A SPB_TRANSFER_BUFFER_LIST_ENTRY  structure that specifies the base address and the length of a simple transfer buffer. Use this member of the union if <b>Format</b> is <b>SpbTransferBufferFormatSimple</b> or <b>SpbTransferBufferFormatSimpleNonPaged</b>. The <b>SpbTransferBufferFormatSimpleNonPaged</b> format is used only by kernel-mode clients.


## -remarks



This structure is used by an <a href="https://msdn.microsoft.com/library/windows/hardware/hh406223">SPB_TRANSFER_LIST_ENTRY</a> structure to describe a transfer buffer.

The <b>Mdl</b> member of this structure can be used only by clients of the SPB controller driver that are kernel-mode components. User-mode clients must not use this member. For more information about MDLs, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565421">Using MDLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh406216">SPB_TRANSFER_BUFFER_FORMAT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406217">SPB_TRANSFER_BUFFER_LIST_ENTRY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406223">SPB_TRANSFER_LIST_ENTRY</a>
 

 

