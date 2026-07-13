---
UID: NS:mswsock._TRANSMIT_FILE_BUFFERS
title: TRANSMIT_FILE_BUFFERS (mswsock.h)
description: The TRANSMIT_FILE_BUFFERS structure (mswsock.h) specifies data to be transmitted before and after file data during a TransmitFile function file transfer operation.
helpviewer_keywords: ["*LPTRANSMIT_FILE_BUFFERS","*PTRANSMIT_FILE_BUFFERS","TRANSMIT_FILE_BUFFERS","TRANSMIT_FILE_BUFFERS structure [Winsock]","_TRANSMIT_FILE_BUFFERS","_win32_transmit_file_buffers_2","mswsock/TRANSMIT_FILE_BUFFERS","winsock.transmit_file_buffers_2"]
old-location: winsock\transmit_file_buffers_2.htm
tech.root: WinSock
ms.assetid: 862dd8f8-5929-4426-b531-a87e36506634
ms.date: 08/12/2022
ms.keywords: '*LPTRANSMIT_FILE_BUFFERS, *PTRANSMIT_FILE_BUFFERS, TRANSMIT_FILE_BUFFERS, TRANSMIT_FILE_BUFFERS structure [Winsock], _TRANSMIT_FILE_BUFFERS, _win32_transmit_file_buffers_2, mswsock/TRANSMIT_FILE_BUFFERS, winsock.transmit_file_buffers_2'
req.header: mswsock.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TRANSMIT_FILE_BUFFERS, *PTRANSMIT_FILE_BUFFERS, *LPTRANSMIT_FILE_BUFFERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRANSMIT_FILE_BUFFERS
 - mswsock/_TRANSMIT_FILE_BUFFERS
 - PTRANSMIT_FILE_BUFFERS
 - mswsock/PTRANSMIT_FILE_BUFFERS
 - TRANSMIT_FILE_BUFFERS
 - mswsock/TRANSMIT_FILE_BUFFERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mswsock.h
api_name:
 - TRANSMIT_FILE_BUFFERS
---

# TRANSMIT_FILE_BUFFERS structure


## -description

The 
<b>TRANSMIT_FILE_BUFFERS</b> structure specifies data to be transmitted before and after file data during a 
<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a> function file transfer operation.

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

<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>
