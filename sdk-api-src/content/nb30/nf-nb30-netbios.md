---
UID: NF:nb30.Netbios
title: Netbios function
author: windows-driver-content
description: The Netbios function interprets and executes the specified network control block (NCB).
old-location: netbios\netbios.htm
old-project: NetBIOS
ms.assetid: 3eadbfa7-53de-4c62-b61b-da84b9da58f7
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: Netbios, Netbios function [NetBIOS], nb30/Netbios, netbios.netbios
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SystemHealthAgentState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	netapi32.dll
api_name:
-	Netbios
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# Netbios function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/library/windows/hardware/dn965731">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>Netbios</b> function interprets and executes the specified network control block (NCB).

The <b>Netbios</b> function is provided primarily for applications that were written for the NetBIOS interface and need to be ported to Windows. Applications not requiring compatibility with NetBIOS should use other interfaces, such as Windows Sockets, mailslots, named pipes, RPC, or distributed COM to accomplish tasks similar to those supported by NetBIOS. These other interfaces are more flexible and portable.


## -parameters




### -param pncb

TBD




#### - pcnb

A  pointer to an <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure that describes the network control block. 



## -returns



For synchronous requests, the return value is the return code in the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure. That value is also returned in the <b>ncb_retcode</b> member of the <b>NCB</b> structure.

For asynchronous requests, there are the following possibilities:

<ul>
<li>If the asynchronous command has already completed when <b>Netbios</b> returns to its caller, the return value is the return code of the NCB structure, just as if it were a synchronous <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure.</li>
<li>If the asynchronous command is still pending when <b>Netbios</b> returns to its caller, the return value is zero.</li>
</ul>
If the address specified by the pncb parameter is invalid, the return value is <b>NRC_BADNCB</b>.

If the buffer length specified in the <b>ncb_length</b> member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure is incorrect, or if the buffer specified by the <b>ncb_retcode</b> member is protected from write operations, the return value is <b>NRC_BUFLEN</b>.




## -remarks



When an asynchronous network control block finishes and the <b>ncb_post</b> member is nonzero, the routine specified in <b>ncb_post</b> is called with a single parameter. This parameter contains a pointer to an <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure, the network control block.

The <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure contains a handle of an event (the <b>ncb_event</b> member). The system sets the event to the nonsignaled state when an asynchronous NetBIOS command is accepted, and sets the event to the signaled state when the asynchronous NetBIOS command is completed. Only manual reset events should be used for synchronization. A specified event should not be associated with more than one active asynchronous NetBIOS command.

Using <b>ncb_event</b> to submit asynchronous requests requires fewer system resources than using <b>ncb_post</b>. Also, when <b>ncb_event</b> is nonzero, the pending request is canceled if the thread terminates before the request is processed. This is not true for requests sent by using <b>ncb_post</b>.




## -see-also




<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>
 

 

