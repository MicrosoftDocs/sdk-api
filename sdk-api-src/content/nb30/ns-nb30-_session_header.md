---
UID: NS:nb30._SESSION_HEADER
title: "_SESSION_HEADER"
author: windows-sdk-content
description: The SESSION_HEADER structure contains information about a network session.
old-location: netbios\session_header.htm
tech.root: NetBIOS
ms.assetid: 0b466bc7-6d20-477f-9e64-1d3dc0744484
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSESSION_HEADER, PSESSION_HEADER, PSESSION_HEADER structure pointer [NetBIOS], SESSION_HEADER, SESSION_HEADER structure [NetBIOS], _SESSION_HEADER, nb30/PSESSION_HEADER, nb30/SESSION_HEADER, netbios.session_header"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - SESSION_HEADER
product: Windows
targetos: Windows
req.typenames: SESSION_HEADER, *PSESSION_HEADER
req.redist: 
---

# _SESSION_HEADER structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>SESSION_HEADER</b> structure contains information about a network session. This structure is pointed to by the <b>ncb_buffer</b> member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure. <b>SESSION_HEADER</b> is followed by as many <a href="https://msdn.microsoft.com/29352074-3dff-430f-82fb-6f7fd0b2966a">SESSION_BUFFER</a> structures as are required to describe the current network sessions.


## -struct-fields




### -field sess_name

Specifies the name number of the session. This value corresponds to the <b>ncb_num</b> member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure. 



### -field num_sess

Specifies the number of sessions that have the name specified by the <b>sess_name</b> member. 



### -field rcv_dg_outstanding

Specifies the number of outstanding <b>NCBDGRECV</b> and <b>NCBDGRECVBC</b> commands. 



### -field rcv_any_outstanding

Specifies the number of outstanding <b>NCBRECVANY</b> commands.


## -see-also




<b></b>



<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>



<a href="https://msdn.microsoft.com/64ef39ec-d69a-4e33-9192-dda6d1bb84b8">NetBIOS Structures</a>



<a href="https://msdn.microsoft.com/29352074-3dff-430f-82fb-6f7fd0b2966a">SESSION_BUFFER</a>



<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">The NetBIOS Interface Overview</a>
 

 

