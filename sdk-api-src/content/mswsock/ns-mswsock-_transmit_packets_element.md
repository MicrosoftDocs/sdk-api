---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _TRANSMIT_PACKETS_ELEMENT structure


## -description


The 
<b>TRANSMIT_PACKETS_ELEMENT</b> structure specifies a single data element to be transmitted by the 
<a href="https://msdn.microsoft.com/c574d320-2a90-40bb-b34c-6023e80514e6">TransmitPackets</a> function.


## -struct-fields




### -field dwElFlags

Type: <b>ULONG</b>

Flags used to describe the contents of the packet array element, and to customize 
<b>TransmitPackets</b> function processing. The following table lists valid flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TP_ELEMENT_FILE"></a><a id="tp_element_file"></a><dl>
<dt><b>TP_ELEMENT_FILE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that data resides in a file. Default setting for <b>dwElFlags</b>. Mutually exclusive with TP_ELEMENT_MEMORY.

</td>
</tr>
<tr>
<td width="40%"><a id="TP_ELEMENT_MEMORY"></a><a id="tp_element_memory"></a><dl>
<dt><b>TP_ELEMENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that data resides in memory. Mutually exclusive with TP_ELEMENT_FILE.

</td>
</tr>
<tr>
<td width="40%"><a id="TP_ELEMENT_EOP"></a><a id="tp_element_eop"></a><dl>
<dt><b>TP_ELEMENT_EOP</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this element should not be combined with the next element in a single 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> request from the sockets layer to the transport. This flag is used for granular control of the content of each message on a datagram or message-oriented socket.

</td>
</tr>
</table>
 


### -field cLength

Type: <b>ULONG</b>

The number of bytes to transmit. If zero, the entire file is transmitted.


### -field nFileOffset

Type: <b>LARGE_INTEGER</b>

The file offset, in bytes, at which to begin the transfer. Valid only if TP_ELEMENT_FILE is specified in <b>dwEIFlags</b>. When set to –1, transmission begins at the current byte offset.


### -field hFile

Type: <b>HANDLE</b>

A handle to an open file to be transmitted. Valid only if TP_ELEMENT_FILE is specified in <b>dwEIFlags</b>. Windows reads the file sequentially; caching performance is improved by opening this handle with FILE_FLAG_SEQUENTIAL_SCAN.


### -field pBuffer

Type: <b>PVOID</b>

A pointer to the data in memory to be sent. Valid only if TP_ELEMENT_MEMORY is specified in <b>dwEIFlags</b>.


## -see-also




<a href="https://msdn.microsoft.com/c574d320-2a90-40bb-b34c-6023e80514e6">TransmitPackets</a>



<a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>



<b>send</b>
 

 

