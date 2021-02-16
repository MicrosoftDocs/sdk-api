---
UID: NS:nb30._FIND_NAME_BUFFER
title: FIND_NAME_BUFFER (nb30.h)
description: The FIND_NAME_BUFFER structure contains information about a local network session.
helpviewer_keywords: ["*PFIND_NAME_BUFFER","FIND_NAME_BUFFER","FIND_NAME_BUFFER structure [NetBIOS]","PFIND_NAME_BUFFER","PFIND_NAME_BUFFER structure pointer [NetBIOS]","nb30/FIND_NAME_BUFFER","nb30/PFIND_NAME_BUFFER","netbios.find_name_buffer"]
old-location: netbios\find_name_buffer.htm
tech.root: NetBIOS
ms.assetid: d35cd375-6207-4019-bd3e-20dc302e9c45
ms.date: 12/05/2018
ms.keywords: '*PFIND_NAME_BUFFER, FIND_NAME_BUFFER, FIND_NAME_BUFFER structure [NetBIOS], PFIND_NAME_BUFFER, PFIND_NAME_BUFFER structure pointer [NetBIOS], nb30/FIND_NAME_BUFFER, nb30/PFIND_NAME_BUFFER, netbios.find_name_buffer'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FIND_NAME_BUFFER, *PFIND_NAME_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FIND_NAME_BUFFER
 - nb30/_FIND_NAME_BUFFER
 - PFIND_NAME_BUFFER
 - nb30/PFIND_NAME_BUFFER
 - FIND_NAME_BUFFER
 - nb30/FIND_NAME_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - FIND_NAME_BUFFER
---

# FIND_NAME_BUFFER structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>FIND_NAME_BUFFER</b> structure contains information about a local network session. One or more <b>FIND_NAME_BUFFER</b> structures follows a <a href="/windows/desktop/api/nb30/ns-nb30-find_name_header">FIND_NAME_HEADER</a> structure when an application specifies the <b>NCBFINDNAME</b> command in the ncb_command member of the <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure.

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



<a href="/windows/desktop/api/nb30/ns-nb30-find_name_header">FIND_NAME_HEADER</a>



<a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a>



<a href="/previous-versions/windows/desktop/netbios/netbios-structures">NetBIOS Structures</a>



<a href="/previous-versions/windows/desktop/netbios/portal">The NetBIOS Interface Overview</a>