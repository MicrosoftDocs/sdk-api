---
UID: NE:spb.SPB_TRANSFER_BUFFER_FORMAT
title: SPB_TRANSFER_BUFFER_FORMAT
author: windows-driver-content
description: The SPB_TRANSFER_BUFFER_FORMAT enumeration specifies the format of the buffer that is described by an SPB_TRANSFER_BUFFER structure.
old-location: spb\spb_transfer_buffer_format.htm
old-project: SPB
ms.assetid: EAC78940-318D-4785-9D7E-410B8AB2F4C7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSPB_TRANSFER_BUFFER_FORMAT, SPB.spb_transfer_buffer_format, SPB_TRANSFER_BUFFER_FORMAT, SPB_TRANSFER_BUFFER_FORMAT enumeration [Buses], SpbTransferBufferFormatInvalid, SpbTransferBufferFormatList, SpbTransferBufferFormatMax, SpbTransferBufferFormatMdl, SpbTransferBufferFormatSimple, SpbTransferBufferFormatSimpleNonPaged, spb/SPB_TRANSFER_BUFFER_FORMAT, spb/SpbTransferBufferFormatInvalid, spb/SpbTransferBufferFormatList, spb/SpbTransferBufferFormatMax, spb/SpbTransferBufferFormatMdl, spb/SpbTransferBufferFormatSimple, spb/SpbTransferBufferFormatSimpleNonPaged"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: spb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SpatialInteractionManagerInterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SPB_TRANSFER_BUFFER_FORMAT, *PSPB_TRANSFER_BUFFER_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Spb.h
api_name:
-	SPB_TRANSFER_BUFFER_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SPB_TRANSFER_BUFFER_FORMAT enumeration


## -description


The <b>SPB_TRANSFER_BUFFER_FORMAT</b> enumeration specifies the format of the buffer that is described by an <a href="https://msdn.microsoft.com/library/windows/hardware/hh406215">SPB_TRANSFER_BUFFER</a> structure.


## -enum-fields




### -field SpbTransferBufferFormatInvalid

Reserved for use by the operating system.


### -field SpbTransferBufferFormatSimple

The transfer buffer is described by a simple user-mode or kernel-mode pointer and a length.


### -field SpbTransferBufferFormatList

The transfer buffer is described by a pointer to a list of buffers and a count of the number of buffers in the list.


### -field SpbTransferBufferFormatSimpleNonPaged

The transfer buffer is described by a simple user-mode or kernel-mode pointer and a length. The buffer resides in nonpaged memory. This format value is valid only if the client that originates the I/O request is a kernel-mode driver.


### -field SpbTransferBufferFormatMdl

The transfer buffer is described by a pointer to an MDL. This format value is valid only if the client that originates the I/O request is a kernel-mode driver.


### -field SpbTransferBufferFormatMax

Reserved for use by the operating system.


## -remarks



The <b>Format</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406215">SPB_TRANSFER_BUFFER</a> structure is an <b>SPB_TRANSFER_BUFFER_FORMAT</b> enumeration value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh406215">SPB_TRANSFER_BUFFER</a>
 

 

