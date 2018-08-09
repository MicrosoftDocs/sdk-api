---
UID: NS:nb30._FIND_NAME_HEADER
title: "_FIND_NAME_HEADER"
author: windows-sdk-content
description: The FIND_NAME_HEADER structure contains information about a network name. This structure is followed by as many FIND_NAME_BUFFER structures as are required to describe the name.
old-location: netbios\find_name_header.htm
old-project: NetBIOS
ms.assetid: 66b0cf77-3c25-4b00-9e9b-abc0442e3831
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "*PFIND_NAME_HEADER, FIND_NAME_HEADER, FIND_NAME_HEADER structure [NetBIOS], PFIND_NAME_HEADER, PFIND_NAME_HEADER structure pointer [NetBIOS], _FIND_NAME_HEADER, nb30/FIND_NAME_HEADER, nb30/PFIND_NAME_HEADER, netbios.find_name_header"
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
req.typenames: FIND_NAME_HEADER, *PFIND_NAME_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - FIND_NAME_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _FIND_NAME_HEADER structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/library/windows/hardware/dn965731">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>FIND_NAME_HEADER</b> structure contains information about a network name. This structure is followed by as many <a href="https://msdn.microsoft.com/d35cd375-6207-4019-bd3e-20dc302e9c45">FIND_NAME_BUFFER</a> structures as are required to describe the name.


## -struct-fields




### -field node_count

Specifies the number of nodes on which the specified name was found. This structure is followed by the number of <a href="https://msdn.microsoft.com/d35cd375-6207-4019-bd3e-20dc302e9c45">FIND_NAME_BUFFER</a> structures specified by the <b>node_count</b> member.


### -field reserved

Reserved


### -field unique_group

Specifies whether the name is unique. This value is 0 to specify a unique name or 1 to specify a group. 



## -remarks



The <b>FIND_NAME_HEADER</b> structure is pointed to by the <b>ncb_buffer</b> member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure when an application issues an <b>NCBFINDNAME</b> command.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/d35cd375-6207-4019-bd3e-20dc302e9c45">FIND_NAME_BUFFER</a>



<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>



<a href="https://msdn.microsoft.com/64ef39ec-d69a-4e33-9192-dda6d1bb84b8">NetBIOS Structures</a>



<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">The NetBIOS Interface Overview</a>
 

 

