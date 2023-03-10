---
UID: NS:nb30._FIND_NAME_HEADER
title: FIND_NAME_HEADER (nb30.h)
description: The FIND_NAME_HEADER structure contains information about a network name. This structure is followed by as many FIND_NAME_BUFFER structures as are required to describe the name.
helpviewer_keywords: ["*PFIND_NAME_HEADER","FIND_NAME_HEADER","FIND_NAME_HEADER structure [NetBIOS]","PFIND_NAME_HEADER","PFIND_NAME_HEADER structure pointer [NetBIOS]","nb30/FIND_NAME_HEADER","nb30/PFIND_NAME_HEADER","netbios.find_name_header"]
old-location: netbios\find_name_header.htm
tech.root: NetBIOS
ms.assetid: 66b0cf77-3c25-4b00-9e9b-abc0442e3831
ms.date: 12/05/2018
ms.keywords: '*PFIND_NAME_HEADER, FIND_NAME_HEADER, FIND_NAME_HEADER structure [NetBIOS], PFIND_NAME_HEADER, PFIND_NAME_HEADER structure pointer [NetBIOS], nb30/FIND_NAME_HEADER, nb30/PFIND_NAME_HEADER, netbios.find_name_header'
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
req.typenames: FIND_NAME_HEADER, *PFIND_NAME_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FIND_NAME_HEADER
 - nb30/_FIND_NAME_HEADER
 - PFIND_NAME_HEADER
 - nb30/PFIND_NAME_HEADER
 - FIND_NAME_HEADER
 - nb30/FIND_NAME_HEADER
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
 - FIND_NAME_HEADER
---

# FIND_NAME_HEADER structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>FIND_NAME_HEADER</b> structure contains information about a network name. This structure is followed by as many <a href="/windows/desktop/api/nb30/ns-nb30-find_name_buffer">FIND_NAME_BUFFER</a> structures as are required to describe the name.

## -struct-fields

### -field node_count

Specifies the number of nodes on which the specified name was found. This structure is followed by the number of <a href="/windows/desktop/api/nb30/ns-nb30-find_name_buffer">FIND_NAME_BUFFER</a> structures specified by the <b>node_count</b> member.

### -field reserved

Reserved

### -field unique_group

Specifies whether the name is unique. This value is 0 to specify a unique name or 1 to specify a group.

## -remarks

The <b>FIND_NAME_HEADER</b> structure is pointed to by the <b>ncb_buffer</b> member of the <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure when an application issues an <b>NCBFINDNAME</b> command.

## -see-also

<b></b>



<a href="/windows/desktop/api/nb30/ns-nb30-find_name_buffer">FIND_NAME_BUFFER</a>



<a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a>



<a href="/previous-versions/windows/desktop/netbios/netbios-structures">NetBIOS Structures</a>



<a href="/previous-versions/windows/desktop/netbios/portal">The NetBIOS Interface Overview</a>