---
UID: NF:traffic.TcEnumerateInterfaces
title: TcEnumerateInterfaces function (traffic.h)
description: The TcEnumerateInterfaces function enumerates all traffic control—enabled network interfaces. Clients are notified of interface changes through the ClNotifyHandler function.
helpviewer_keywords: ["TcEnumerateInterfaces","TcEnumerateInterfaces function [QOS]","_gqos_tcenumerateinterfaces","qos.tcenumerateinterfaces","traffic/TcEnumerateInterfaces"]
old-location: qos\tcenumerateinterfaces.htm
tech.root: QOS
ms.assetid: e6fbaa17-6b4b-45a2-baf7-898864a797b7
ms.date: 12/05/2018
ms.keywords: TcEnumerateInterfaces, TcEnumerateInterfaces function [QOS], _gqos_tcenumerateinterfaces, qos.tcenumerateinterfaces, traffic/TcEnumerateInterfaces
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
 - TcEnumerateInterfaces
 - traffic/TcEnumerateInterfaces
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
 - TcEnumerateInterfaces
---

# TcEnumerateInterfaces function


## -description

The 
<b>TcEnumerateInterfaces</b> function enumerates all traffic control–enabled network interfaces. Clients are notified of interface changes through the 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a> function.

## -parameters

### -param ClientHandle [in]

Handle used by traffic control to identify the client. Clients receive handles when registering with traffic control through the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a> function.

### -param pBufferSize [in, out]

Pointer to a value indicating the size of the buffer. For input, this value is the size of the buffer, in bytes, allocated by the caller. For output, this value is the actual size of the buffer, in bytes, used or needed by traffic control. A value of zero on output indicates that no traffic control interfaces are available, indicating that the QOS Packet Scheduler is not installed.

### -param InterfaceBuffer [out]

Pointer to the buffer containing the returned list of interface descriptors.

## -returns

Successful completion returns the device name of the interface.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The client handle is invalid.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to enumerate all interfaces. If this error is returned, the correct (required) size of the buffer is passed back in <i>pBufferSize</i>.

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
</table>

## -remarks

The client calling the 
<b>TcEnumerateInterfaces</b> function must first allocate a buffer, then pass the buffer to traffic control through <i>InterfaceBuffer</i>. Traffic control returns a pointer to an array of interface descriptors in <i>InterfaceBuffer</i>. Each interface descriptor contains two elements:

<ul>
<li>The traffic control interface's identifying text string.</li>
<li>The network address list descriptor currently associated with the interface.</li>
</ul>
The network address list descriptor includes the media type, as well as a list of network addresses. The media type determines how the network address list should be interpreted:

<ul>
<li>For connectionless media such as a LAN, the network address list contains all the protocol-specific addresses associated with the interface.</li>
<li>For connection-oriented media such as a WAN, the network address list contains an even number of network addresses: 


<ul>
<li>The first address in each pair represents the local (source) address of the interface.</li>
<li>The second address in each pair represents the remote (destination) address of the interface.</li>
</ul>
</li>
</ul>
<div class="alert"><b>Note</b>  Use of the 
<b>TcEnumerateInterfaces</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a>