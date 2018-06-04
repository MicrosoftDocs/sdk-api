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
 

 

