---
UID: NS:nb30._FIND_NAME_BUFFER
title: "_FIND_NAME_BUFFER"
author: windows-sdk-content
description: The FIND_NAME_BUFFER structure contains information about a local network session.
old-location: netbios\find_name_buffer.htm
old-project: NetBIOS
ms.assetid: d35cd375-6207-4019-bd3e-20dc302e9c45
ms.author: windowssdkdev
ms.date: 05/02/2018
ms.keywords: "*PFIND_NAME_BUFFER, FIND_NAME_BUFFER, FIND_NAME_BUFFER structure [NetBIOS], PFIND_NAME_BUFFER, PFIND_NAME_BUFFER structure pointer [NetBIOS], _FIND_NAME_BUFFER, nb30/FIND_NAME_BUFFER, nb30/PFIND_NAME_BUFFER, netbios.find_name_buffer"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: nb30.h
req.include-header: 
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
tech.root: 
req.typenames: FIND_NAME_BUFFER, *PFIND_NAME_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Nb30.h
api_name:
-	FIND_NAME_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _FIND_NAME_BUFFER structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/library/windows/hardware/dn965731">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>FIND_NAME_BUFFER</b> structure contains information about a local network session. One or more <b>FIND_NAME_BUFFER</b> structures follows a <a href="https://msdn.microsoft.com/66b0cf77-3c25-4b00-9e9b-abc0442e3831">FIND_NAME_HEADER</a> structure when an application specifies the <b>NCBFINDNAME</b> command in the ncb_command member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure. 


## -struct-fields




### -field length

Specifies the length, in bytes, of the <b>FIND_NAME_BUFFER</b> structure. Although this structure always occupies 33 bytes, not all of the structure is necessarily valid.


### -field access_control

Specifies the access control for the LAN header.


### -field frame_control

Specifies the frame control for the LAN header.


### -field destination_addr

Specifies the destination address of the remote node where the name was found.


### -field source_addr

Specifies the source address for the remote node where the name was found.


### -field routing_info

Specifies additional routing information.


## -see-also




<b></b>



<a href="https://msdn.microsoft.com/66b0cf77-3c25-4b00-9e9b-abc0442e3831">FIND_NAME_HEADER</a>



<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>



<a href="https://msdn.microsoft.com/64ef39ec-d69a-4e33-9192-dda6d1bb84b8">NetBIOS Structures</a>



<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">The NetBIOS Interface Overview</a>
 

 

