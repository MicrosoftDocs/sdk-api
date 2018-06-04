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
 

 

