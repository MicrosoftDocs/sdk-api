---
UID: NF:traffic.TcRegisterClient
title: TcRegisterClient function (traffic.h)
description: The TcRegisterClient function is used to register a client with the traffic control interface (TCI). The TcRegisterClient function must be the first function call a client makes to the TCI.
helpviewer_keywords: ["TcRegisterClient","TcRegisterClient function [QOS]","_gqos_tcregisterclient","qos.tcregisterclient","traffic/TcRegisterClient"]
old-location: qos\tcregisterclient.htm
tech.root: QOS
ms.assetid: 10bbc08d-4bfa-4a64-b5b8-b720d7bc3185
ms.date: 12/05/2018
ms.keywords: TcRegisterClient, TcRegisterClient function [QOS], _gqos_tcregisterclient, qos.tcregisterclient, traffic/TcRegisterClient
req.header: traffic.h
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
req.lib: Traffic.lib
req.dll: Traffic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TcRegisterClient
 - traffic/TcRegisterClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Traffic.dll
api_name:
 - TcRegisterClient
---

# TcRegisterClient function


## -description

The 
<b>TcRegisterClient</b> function is used to register a client with the traffic control interface (TCI). The 
<b>TcRegisterClient</b> function must be the first function call a client makes to the TCI.

Client registration provides callback routines that allow the TCI to complete either client-initiated operations or asynchronous events. Upon successful registration, the caller of the 
<b>TcRegisterClient</b> function must be ready to have any of its TCI handlers called. See 
<a href="/previous-versions/windows/desktop/qos/entry-points-exposed-by-clients-of-the-traffic-control-interface">Entry Points Exposed by Clients of the Traffic Control Interface</a> for more information.

## -parameters

### -param TciVersion [in]

Traffic control version expected by the client, included to ensure compatibility between traffic control and the client. Clients can pass CURRENT_TCI_VERSION, defined in Traffic.h.

### -param ClRegCtx [in]

Client registration context. <i>ClRegCtx</i> is returned when the client's notification handler function is called. This can be a container to hold an arbitrary client-defined context for this instance of the interface.

### -param ClientHandlerList [in]

Pointer to a list of client-supplied handlers. Client-supplied handlers are used for notification events and asynchronous completions. Each completion routine is optional, with the exception of the notification handler. Setting the notification handler to <b>NULL</b> will return an ERROR_INVALID_PARAMETER.

### -param pClientHandle [out]

Pointer to the buffer that traffic control uses to return a registration handle to the client.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INCOMPATIBLE_TCI_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The TCI version is wrong.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Traffic control failed to open a system device. The likely cause is insufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TOO_MANY_CLIENTS</b></dt>
</dl>
</td>
<td width="60%">
Traffic Control was unable to register with the kernel component GPC. The likely cause is too many traffic control clients are currently connected.

<b>Windows 2000:  </b>This value is not supported.

</td>
</tr>
</table>

## -remarks

Some of the return codes can be found in tcerror.h.

<div class="alert"><b>Note</b>  Use of the 
<b>TcRegisterClient</b> function requires administrative privilege.</div>
<div> </div>