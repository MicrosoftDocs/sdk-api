---
UID: NF:winusb.WinUsb_ReadIsochPipe
title: WinUsb_ReadIsochPipe function (winusb.h)
description: The WinUsb_ReadIsochPipe function reads data from an isochronous OUT endpoint.
helpviewer_keywords: ["WinUsb_ReadIsochPipe","WinUsb_ReadIsochPipe function [Buses]","buses.winusb_readisochpipe","winusb/WinUsb_ReadIsochPipe"]
old-location: buses\winusb_readisochpipe.htm
tech.root: buses
ms.assetid: B8FE9DC4-AB3D-4389-BC2A-9572CE1C8F91
ms.date: 12/05/2018
ms.keywords: WinUsb_ReadIsochPipe, WinUsb_ReadIsochPipe function [Buses], buses.winusb_readisochpipe, winusb/WinUsb_ReadIsochPipe
req.header: winusb.h
req.include-header: Winusb.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinUsb_ReadIsochPipe
 - winusb/WinUsb_ReadIsochPipe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_ReadIsochPipe
---

# WinUsb_ReadIsochPipe function


## -description

The <b>WinUsb_ReadIsochPipe</b> function reads data from an isochronous IN endpoint.

## -parameters

### -param BufferHandle [in]

An opaque handle to the transfer buffer that was registered by a previous call to <a href="/windows/desktop/api/winusb/nf-winusb-winusb_registerisochbuffer">WinUsb_RegisterIsochBuffer</a>.

### -param Offset [in]

Offset into the buffer relative to the start the transfer.

### -param Length [in]

Length in bytes of the transfer buffer.

### -param FrameNumber [in, out]

On input, indicates the starting frame number for the transfer. On output, contains the frame number of the frame that follows the last frame used in the transfer.

### -param NumberOfPackets [in]

Total number of isochronous packets required to hold the transfer buffer. Also indicates the number of elements in the array pointed to by <i>IsoPacketDescriptors</i>.

### -param IsoPacketDescriptors [out]

An array of <a href="/windows-hardware/drivers/ddi/content/usb/ns-usb-_usbd_iso_packet_descriptor">USBD_ISO_PACKET_DESCRIPTOR</a> structures.  After the transfer completes, each element contains the status and size of the isochronous packet.

### -param Overlapped [in, optional]

Pointer to an <a href="/windows/desktop/api/shobjidl/ns-shobjidl-overlapped">OVERLAPPED</a> structure used for asynchronous operations.

## -returns

<b>WinUsb_ReadIsochPipe</b> returns TRUE if the operation succeeds. Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.

## -remarks

<b>WinUsb_ReadIsochPipe</b> packetizes the transfer buffer so that in each 1ms interval, the host can receive the maximum bytes allowed per interval. The maximum bytes is as specified by the endpoint descriptor for full and high-speed endpoints, and endpoint companion descriptor for SuperSpeed endpoints.
If the caller submits multiple read requests to stream data from the device, the transfer size should be a multiple of the maximum bytes per interval (as returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_querypipeex">WinUsb_QueryPipeEx</a>) * 8 / interval.


Because of the transfer packaging used in the underlying kernel-mode interface, the lowest latency notification to an application or driver is 1ms intervals.

## -see-also

<a href="/windows-hardware/drivers/usbcon/">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>
