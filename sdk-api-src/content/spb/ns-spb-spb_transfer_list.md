---
UID: NS:spb.SPB_TRANSFER_LIST
title: SPB_TRANSFER_LIST
author: windows-driver-content
description: The SPB_TRANSFER_LIST structure describes an I/O transfer sequence.
old-location: spb\spb_transfer_list.htm
old-project: SPB
ms.assetid: DC4E165B-4D3A-4C5F-9B6F-8CB825BAF4FD
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSPB_TRANSFER_LIST, PSPB_TRANSFER_LIST, PSPB_TRANSFER_LIST structure pointer [Buses], SPB.spb_transfer_list, SPB_TRANSFER_LIST, SPB_TRANSFER_LIST structure [Buses], spb/PSPB_TRANSFER_LIST, spb/SPB_TRANSFER_LIST"
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
req.typenames: SPB_TRANSFER_LIST, *PSPB_TRANSFER_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Spb.h
api_name:
-	SPB_TRANSFER_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SPB_TRANSFER_LIST structure


## -description


The <b>SPB_TRANSFER_LIST</b> structure describes an <a href="https://msdn.microsoft.com/7415DB28-5E93-4F47-B169-7C652969D4C7">I/O transfer sequence</a>.


## -struct-fields




### -field Size

The size, in bytes, of the <b>SPB_TRANSFER_LIST</b> structure. This size value does not include any <b>Transfers</b> array elements that might follow this structure. If new members are added to future versions of this structure, the <b>Size</b> value can be used to determine which version of the <b>SPB_TRANSFER_LIST</b> structure is being used.


### -field Reserved

Reserved for use by the operating system. Set to zero.


### -field TransferCount

The number of elements in the <b>Transfers</b> array. This array contains a minimum of one element.


### -field Transfers

This member is the first element in an array of <a href="https://msdn.microsoft.com/library/windows/hardware/hh406223">SPB_TRANSFER_LIST_ENTRY</a> structures.  Each array element describes an individual transfer in the I/O transfer sequence. If the array contains more than one element, the additional array elements immediately follow the <b>SPB_TRANSFER_LIST</b> structure in memory. The transfers are performed in the order in which they appear in the array, starting with the first element.


## -remarks



The input buffer for an <a href="https://msdn.microsoft.com/library/windows/hardware/hh450857">IOCTL_SPB_EXECUTE_SEQUENCE</a> request begins with an <b>SPB_TRANSFER_LIST</b> structure. The first transfer in the requested I/O transfer sequence is specified in the <b>Transfers</b> member of this structure. If the sequence contains more than one transfer, the array elements that describe the additional transfers immediately follow the <b>SPB_TRANSFER_LIST</b> structure.

The input buffer for an <a href="https://msdn.microsoft.com/library/windows/hardware/hh974774">IOCTL_SPB_FULL_DUPLEX</a> request begins with an <b>SPB_TRANSFER_LIST</b> structure. The <b>SPB_TRANSFER_LIST</b> structure for this request always specifies two buffers. The first buffer, which is described by the <b>Transfers</b> member of this structure, contains the data to write to the device. The second buffer, which is described by an array element that immediately follows the <b>SPB_TRANSFER_LIST</b> structure, is used to hold the data read from the device.

If your SPB controller driver supports custom I/O control (IOCTL) requests that use input or output buffers, use the <b>SPB_TRANSFER_LIST</b> structure to describe these buffers. For more information, see <a href="https://msdn.microsoft.com/577122CC-D1F8-41C5-BE77-A22FC8516B82">Using the SPB_TRANSFER_LIST Structure for Custom IOCTLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450857">IOCTL_SPB_EXECUTE_SEQUENCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh974774">IOCTL_SPB_FULL_DUPLEX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406223">SPB_TRANSFER_LIST_ENTRY</a>
 

 

