---
UID: NS:pchannel.tagCHANNEL_DEF
title: tagCHANNEL_DEF
author: windows-sdk-content
description: Contains the name and options of a Remote Desktop Services virtual channel.
old-location: termserv\channel_def_str.htm
old-project: TermServ
ms.assetid: 05fb703f-b43c-420f-aab5-b2d6533a6cab
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CHANNEL_DEF, CHANNEL_DEF structure [Remote Desktop Services], CHANNEL_OPTION_COMPRESS, CHANNEL_OPTION_COMPRESS_RDP, CHANNEL_OPTION_ENCRYPT_CS, CHANNEL_OPTION_ENCRYPT_RDP, CHANNEL_OPTION_ENCRYPT_SC, CHANNEL_OPTION_INITIALIZED, CHANNEL_OPTION_PRI_HIGH, CHANNEL_OPTION_PRI_LOW, CHANNEL_OPTION_PRI_MED, CHANNEL_OPTION_REMOTE_CONTROL_PERSISTENT, CHANNEL_OPTION_SHOW_PROTOCOL, PAL_PACKED_STRUCT, PCHANNEL_DEF, PCHANNEL_DEF structure pointer [Remote Desktop Services], PPCHANNEL_DEF, PPCHANNEL_DEF structure pointer [Remote Desktop Services], _win32_channel_def_str, pchannel/CHANNEL_DEF, pchannel/PCHANNEL_DEF, pchannel/PPCHANNEL_DEF, tagCHANNEL_DEF, termserv.channel_def_str
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
req.typenames: PAL_PACKED_STRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pchannel.h
api_name:
 - CHANNEL_DEF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

