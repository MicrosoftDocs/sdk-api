---
UID: NS:nb30._SESSION_HEADER
title: SESSION_HEADER (nb30.h)

description: The SESSION_HEADER structure contains information about a network session.
old-location: netbios\session_header.htm
tech.root: NetBIOS
ms.assetid: 0b466bc7-6d20-477f-9e64-1d3dc0744484

ms.date: 12/05/2018
ms.keywords: '*PSESSION_HEADER, PSESSION_HEADER, PSESSION_HEADER structure pointer [NetBIOS], SESSION_HEADER, SESSION_HEADER structure [NetBIOS], _SESSION_HEADER, nb30/PSESSION_HEADER, nb30/SESSION_HEADER, netbios.session_header'
ms.topic: struct
f1_keywords:
- nb30/SESSION_HEADER
dev_langs:
 - c++
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
targetos: Windows
req.typenames: SESSION_HEADER, *PSESSION_HEADER
req.redist: 
ms.custom: 19H1
---

# SESSION_HEADER structure


## -description


<p class="CCE_Message">[<a href="https://docs.microsoft.com/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>SESSION_HEADER</b> structure contains information about a network session. This structure is pointed to by the <b>ncb_buffer</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure. <b>SESSION_HEADER</b> is followed by as many <a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-session_buffer">SESSION_BUFFER</a> structures as are required to describe the current network sessions.


## -struct-fields




### -field sess_name

Specifies the name number of the session. This value corresponds to the <b>ncb_num</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure. 



### -field num_sess

Specifies the number of sessions that have the name specified by the <b>sess_name</b> member. 



### -field rcv_dg_outstanding

Specifies the number of outstanding <b>NCBDGRECV</b> and <b>NCBDGRECVBC</b> commands. 



### -field rcv_any_outstanding

Specifies the number of outstanding <b>NCBRECVANY</b> commands.


## -see-also




<b></b>



<a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/netbios/netbios-structures">NetBIOS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-session_buffer">SESSION_BUFFER</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/netbios/portal">The NetBIOS Interface Overview</a>
 

 

