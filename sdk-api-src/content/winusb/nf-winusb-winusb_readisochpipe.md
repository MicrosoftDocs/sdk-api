---
UID: NF:winusb.WinUsb_ReadIsochPipe
title: WinUsb_ReadIsochPipe function (winusb.h)
author: windows-sdk-content
description: The WinUsb_ReadIsochPipe function reads data from an isochronous OUT endpoint.
old-location: buses\winusb_readisochpipe.htm
tech.root: usbref
ms.assetid: B8FE9DC4-AB3D-4389-BC2A-9572CE1C8F91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WinUsb_ReadIsochPipe, WinUsb_ReadIsochPipe function [Buses], buses.winusb_readisochpipe, winusb/WinUsb_ReadIsochPipe
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_ReadIsochPipe
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WinUsb_ReadIsochPipe function


## -description


The <b>WinUsb_ReadIsochPipe</b> function reads data from an isochronous OUT endpoint.  


## -parameters




### -param BufferHandle [in]

An opaque handle to the transfer buffer that was registered by a previous call to <a href="https://msdn.microsoft.com/7781BD59-3576-4C43-9459-E2455F97E9DE">WinUsb_RegisterIsochBuffer</a>. 


### -param Offset [in]

Offset into the buffer relative to the start the transfer.


### -param Length [in]

Length in bytes of the transfer buffer.


### -param FrameNumber [in, out]

On input, indicates the starting frame number for the transfer.  On output, contains the frame number of the frame that follows the last frame used in the transfer.


### -param NumberOfPackets [in]

Total number of isochronous packets required to hold the transfer buffer. Also indicates the number of elements in the array pointed to by <i>IsoPacketDescriptors</i>.


### -param IsoPacketDescriptors [out]

An array of <a href="https://msdn.microsoft.com/45ceff8e-a013-45de-be2e-42c6ca30147e">USBD_ISO_PACKET_DESCRIPTOR</a> structures.  After the transfer completes, each element contains the status and size of the isochronous packet.


### -param Overlapped [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/2b5964e5-dfc8-44f9-86a7-5ea5acc68c1b">OVERLAPPED</a> structure used for asynchronous operations.


## -returns



<b>WinUsb_ReadIsochPipe</b> returns TRUE if the operation succeeds.  Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.




## -remarks



<b>WinUsb_ReadIsochPipe</b> packetizes the transfer buffer so that in each interval,  the host can receive the maximum bytes allowed per interval. The maximum bytes is as specified by the endpoint descriptor for full and high-speed endpoints, and endpoint companion descriptor for SuperSpeed endpoints.
If the caller submits multiple read requests to stream data from the device, the transfer size should be a multiple of the maximum bytes per interval (as returned by <a href="https://msdn.microsoft.com/73C291EC-2345-454B-BC7C-8A443DDFF57C">WinUsb_QueryPipeEx</a>) * 8 / interval.





## -see-also




<a href="https://msdn.microsoft.com/E850ACF2-7FF7-42A2-B3FA-3CFE3A3968E3">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>
 

 

