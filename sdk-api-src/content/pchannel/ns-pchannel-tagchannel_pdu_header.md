---
UID: NS:pchannel.tagCHANNEL_PDU_HEADER
title: tagCHANNEL_PDU_HEADER
author: windows-sdk-content
description: Contains information about a data block being received by the server end of a virtual channel.
old-location: termserv\channel_pdu_header_str.htm
old-project: TermServ
ms.assetid: f980e746-fc05-45e8-af27-6f137ef01bf9
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PCHANNEL_PDU_HEADER, CHANNEL_FLAG_FIRST, CHANNEL_FLAG_LAST, CHANNEL_FLAG_MIDDLE, CHANNEL_FLAG_ONLY, CHANNEL_PDU_HEADER, CHANNEL_PDU_HEADER structure [Remote Desktop Services], PCHANNEL_PDU_HEADER, PCHANNEL_PDU_HEADER structure pointer [Remote Desktop Services], _win32_channel_pdu_header_str, pchannel/CHANNEL_PDU_HEADER, pchannel/PCHANNEL_PDU_HEADER, tagCHANNEL_PDU_HEADER, termserv.channel_pdu_header_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: pchannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pchannel.h
api_name:
 - CHANNEL_PDU_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagCHANNEL_PDU_HEADER structure


## -description


Contains information about a data block being received by the server end of a virtual channel.


## -struct-fields




### -field length

Size, in bytes, of the data block, excluding this header.


### -field flags

Information about the data block. The following bit flags will be set. Note that you should not make direct 
      comparisons using the '==' operator when comparing the values in the following list; instead, use the comparison 
      methods described in the list.



#### CHANNEL_FLAG_FIRST (1)

The chunk is the beginning of the data written by a single write operation.

Use bitwise comparisons when comparing this flag.



#### CHANNEL_FLAG_LAST (2)

The chunk is the end of the data written by a single write operation.

Use bitwise comparisons when comparing this flag.



#### CHANNEL_FLAG_MIDDLE (0)

This is the default. The chunk is in the middle of a block of data written by a single write operation.

Do not use bitwise comparisons to compare this flag value directly. Instead, use bitwise comparisons to 
         determine that the flag value is not <b>CHANNEL_FLAG_FIRST</b> or 
         <b>CHANNEL_FLAG_LAST</b>. This is done by using the following comparison:

<code>Result = !(flags &amp; CHANNEL_FLAG_FIRST) &amp;&amp; !(flags &amp; CHANNEL_FLAG_LAST)</code>



#### CHANNEL_FLAG_ONLY (3)

Combines the <b>CHANNEL_FLAG_FIRST</b> and <b>CHANNEL_FLAG_LAST</b>
          values. The chunk contains all the data from a single write operation.

Use bitwise comparisons when comparing this flag.


## -remarks



In certain cases, Remote Desktop Services places a 
    <b>CHANNEL_PDU_HEADER</b> structure at the beginning 
    of each chunk of data read by a call to the 
    <a href="https://msdn.microsoft.com/7434e761-303f-496f-81cb-83c199ddec8a">WTSVirtualChannelRead</a> function. This will 
    occur if the client DLL sets the <b>CHANNEL_OPTION_SHOW_PROTOCOL</b> option when it calls the 
    <a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a> function to initialize the 
    virtual channel. This will also occur if the channel is a dynamic virtual channel written to by using the 
    <a href="https://msdn.microsoft.com/fef7067c-6d81-42b7-8534-191bc98906d4">IWTSVirtualChannel::Write</a> method.




## -see-also




<a href="https://msdn.microsoft.com/fef7067c-6d81-42b7-8534-191bc98906d4">IWTSVirtualChannel::Write</a>



<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a>



<a href="https://msdn.microsoft.com/bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab">VirtualChannelWrite</a>



<a href="https://msdn.microsoft.com/7434e761-303f-496f-81cb-83c199ddec8a">WTSVirtualChannelRead</a>
 

 

