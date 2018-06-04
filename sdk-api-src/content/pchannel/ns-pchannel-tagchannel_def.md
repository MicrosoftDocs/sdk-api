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

# tagCHANNEL_DEF structure


## -description


Contains the name and options of a Remote Desktop Services 
    virtual channel. A client DLL uses this structure when it calls the 
    <a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a> function to register a 
    virtual channel name.


## -struct-fields




### -field name

A null-terminated string containing the name of a virtual channel. Virtual channel names can contain from 1 
      to <b>CHANNEL_NAME_LEN</b> (7) characters.


### -field options

Specifies the options for this virtual channel. This member can be a combination of the following 
      values.



#### CHANNEL_OPTION_INITIALIZED (0x80000000)

The channel is initialized. This value is set by the 
        <a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a> 
        function.



#### CHANNEL_OPTION_ENCRYPT_RDP (0x40000000)

Encrypt according to 
       <a href="https://msdn.microsoft.com/442c3c7f-d04b-4dcd-945d-f6e0168c59d5">Remote Desktop Protocol</a> (RDP) data 
        encryption (that is, if RDP data is encrypted, do so for this channel, too).



#### CHANNEL_OPTION_ENCRYPT_SC (0x20000000)

Encrypt server-to-client data.



#### CHANNEL_OPTION_ENCRYPT_CS (0x10000000)

Encrypt client-to-server data.



#### CHANNEL_OPTION_PRI_HIGH (0x08000000)

Channel data should be sent with high Multipoint Communications Services (MCS) priority.



#### CHANNEL_OPTION_PRI_MED (0x04000000)

Channel data should be sent with medium MCS priority.



#### CHANNEL_OPTION_PRI_LOW (0x02000000)

Channel data should be sent with low MCS priority.



#### CHANNEL_OPTION_COMPRESS_RDP (0x00800000)

Virtual channel data should be compressed if RDP data is being compressed.



#### CHANNEL_OPTION_COMPRESS (0x00400000)

Virtual channel data should be compressed, regardless of Remote Desktop Protocol (RDP) compression.



#### CHANNEL_OPTION_SHOW_PROTOCOL (0x00200000)

Affects how data sent by the 
        <a href="https://msdn.microsoft.com/bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab">VirtualChannelWrite</a> function is received 
        at the server end. If this value is set, each data block is preceded by a 
        <a href="https://msdn.microsoft.com/f980e746-fc05-45e8-af27-6f137ef01bf9">CHANNEL_PDU_HEADER</a> structure. If this 
        value is not set, the data block includes only the data specified to 
        <b>VirtualChannelWrite</b>.



#### CHANNEL_OPTION_REMOTE_CONTROL_PERSISTENT (0x00100000)

The channel is declared as remote control persistent. This means that the channel will not be closed when 
        a remote control connects to or disconnects from the session connected to the client. For more information, 
        see <a href="https://msdn.microsoft.com/0c3d5429-250e-4272-8cdd-69097acfaff4">Remote Control Persistent 
        Virtual Channels</a>.


## -see-also




<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a>



<a href="https://msdn.microsoft.com/bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab">VirtualChannelWrite</a>
 

 

