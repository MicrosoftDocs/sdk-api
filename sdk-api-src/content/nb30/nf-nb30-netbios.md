---
UID: NF:nb30.Netbios
title: Netbios function (nb30.h)
description: The Netbios function interprets and executes the specified network control block (NCB).
helpviewer_keywords: ["Netbios","Netbios function [NetBIOS]","nb30/Netbios","netbios.netbios"]
old-location: netbios\netbios.htm
tech.root: NetBIOS
ms.assetid: 3eadbfa7-53de-4c62-b61b-da84b9da58f7
ms.date: 12/05/2018
ms.keywords: Netbios, Netbios function [NetBIOS], nb30/Netbios, netbios.netbios
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Netbios
 - nb30/Netbios
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-net-netbios-l1-1-0.dll
 - netapi32.dll
api_name:
 - Netbios
---

# Netbios function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>Netbios</b> function interprets and executes the specified network control block (NCB).

The <b>Netbios</b> function is provided primarily for applications that were written for the NetBIOS interface and need to be ported to Windows. Applications not requiring compatibility with NetBIOS should use other interfaces, such as Windows Sockets, mailslots, named pipes, RPC, or distributed COM to accomplish tasks similar to those supported by NetBIOS. These other interfaces are more flexible and portable.

## -parameters

### -param pncb

A  pointer to an <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure that describes the network control block.

## -returns

For synchronous requests, the return value is the return code in the <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure. That value is also returned in the <b>ncb_retcode</b> member of the <b>NCB</b> structure.

For asynchronous requests, there are the following possibilities:

<ul>
<li>If the asynchronous command has already completed when <b>Netbios</b> returns to its caller, the return value is the return code of the NCB structure, just as if it were a synchronous <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure.</li>
<li>If the asynchronous command is still pending when <b>Netbios</b> returns to its caller, the return value is zero.</li>
</ul>
If the address specified by the pncb parameter is invalid, the return value is <b>NRC_BADNCB</b>.

If the buffer length specified in the <b>ncb_length</b> member of the <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure is incorrect, or if the buffer specified by the <b>ncb_retcode</b> member is protected from write operations, the return value is <b>NRC_BUFLEN</b>.

## -remarks

When an asynchronous network control block finishes and the <b>ncb_post</b> member is nonzero, the routine specified in <b>ncb_post</b> is called with a single parameter. This parameter contains a pointer to an <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure, the network control block.

The <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure contains a handle of an event (the <b>ncb_event</b> member). The system sets the event to the nonsignaled state when an asynchronous NetBIOS command is accepted, and sets the event to the signaled state when the asynchronous NetBIOS command is completed. Only manual reset events should be used for synchronization. A specified event should not be associated with more than one active asynchronous NetBIOS command.

Using <b>ncb_event</b> to submit asynchronous requests requires fewer system resources than using <b>ncb_post</b>. Also, when <b>ncb_event</b> is nonzero, the pending request is canceled if the thread terminates before the request is processed. This is not true for requests sent by using <b>ncb_post</b>.

## -see-also

<a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a>