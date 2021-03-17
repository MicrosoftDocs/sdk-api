---
UID: NF:netfw.INetFwOpenPorts.Remove
title: INetFwOpenPorts::Remove (netfw.h)
description: Closes a port and removes it from the collection.
helpviewer_keywords: ["INetFwOpenPorts interface [ICS/ICF]","Remove method","INetFwOpenPorts.Remove","INetFwOpenPorts::Remove","Remove","Remove method [ICS/ICF]","Remove method [ICS/ICF]","INetFwOpenPorts interface","ics.inetfwopenports_remove","netfw/INetFwOpenPorts::Remove"]
old-location: ics\inetfwopenports_remove.htm
tech.root: ics
ms.assetid: e3719087-f7b9-4780-a030-0c568248080d
ms.date: 12/05/2018
ms.keywords: INetFwOpenPorts interface [ICS/ICF],Remove method, INetFwOpenPorts.Remove, INetFwOpenPorts::Remove, Remove, Remove method [ICS/ICF], Remove method [ICS/ICF],INetFwOpenPorts interface, ics.inetfwopenports_remove, netfw/INetFwOpenPorts::Remove
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwOpenPorts::Remove
 - netfw/INetFwOpenPorts::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwOpenPorts.Remove
---

# INetFwOpenPorts::Remove


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Closes a port and removes it from the collection.

## -parameters

### -param portNumber [in]

Port number to remove.

### -param ipProtocol [in]

Protocol of the port to remove.

## -returns

<h3>C++</h3>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
</table>
 

<h3>VB</h3>
If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
</table>

## -remarks

If the port is already
   closed ,the <b>Remove</b> method has no effect.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFwOpenPorts</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_protocol">NET_FW_IP_PROTOCOL</a>