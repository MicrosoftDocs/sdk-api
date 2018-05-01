---
UID: NS:winsock._TRANSMIT_FILE_BUFFERS
title: "_TRANSMIT_FILE_BUFFERS"
author: windows-driver-content
description: The TRANSMIT_FILE_BUFFERS structure specifies data to be transmitted before and after file data during a TransmitFile function file transfer operation.
old-location: winsock\transmit_file_buffers_2.htm
old-project: WinSock
ms.assetid: 862dd8f8-5929-4426-b531-a87e36506634
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*LPTRANSMIT_FILE_BUFFERS, *PTRANSMIT_FILE_BUFFERS, TRANSMIT_FILE_BUFFERS, TRANSMIT_FILE_BUFFERS structure [Winsock], _TRANSMIT_FILE_BUFFERS, _win32_transmit_file_buffers_2, mswsock/TRANSMIT_FILE_BUFFERS, winsock.transmit_file_buffers_2"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsock.h
req.include-header: Winsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRANSMIT_FILE_BUFFERS, *PTRANSMIT_FILE_BUFFERS, *LPTRANSMIT_FILE_BUFFERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mswsock.h
api_name:
-	TRANSMIT_FILE_BUFFERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _TRANSMIT_FILE_BUFFERS structure


## -description



			The 
<b>TRANSMIT_FILE_BUFFERS</b> structure specifies data to be transmitted before and after file data during a 
<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a> function file transfer operation.


## -struct-fields




### -field Head

Pointer to a buffer that contains data to be transmitted before the file data is transmitted.


### -field HeadLength

Size of the buffer pointed to by <b>Head</b>, in bytes, to be transmitted.


### -field Tail

Pointer to a buffer that contains data to be transmitted after the file data is transmitted.


### -field TailLength

Size of the buffer pointed to <b>Tail</b>, in bytes, to be transmitted.


## -see-also




<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>
 

 

