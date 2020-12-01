---
UID: NF:netfw.INetFwOpenPorts.Item
title: INetFwOpenPorts::Item (netfw.h)
description: Returns the specified port if it is in the collection.
helpviewer_keywords: ["INetFwOpenPorts interface [ICS/ICF]","Item method","INetFwOpenPorts.Item","INetFwOpenPorts::Item","Item","Item method [ICS/ICF]","Item method [ICS/ICF]","INetFwOpenPorts interface","ics.inetfwopenports_item","netfw/INetFwOpenPorts::Item"]
old-location: ics\inetfwopenports_item.htm
tech.root: ics
ms.assetid: f0491047-d20d-49e4-9319-421b48feca48
ms.date: 12/05/2018
ms.keywords: INetFwOpenPorts interface [ICS/ICF],Item method, INetFwOpenPorts.Item, INetFwOpenPorts::Item, Item, Item method [ICS/ICF], Item method [ICS/ICF],INetFwOpenPorts interface, ics.inetfwopenports_item, netfw/INetFwOpenPorts::Item
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
 - INetFwOpenPorts::Item
 - netfw/INetFwOpenPorts::Item
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
 - INetFwOpenPorts.Item
---

# INetFwOpenPorts::Item


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Returns the specified port if it is in the collection.

## -parameters

### -param portNumber [in]

Port number to find.

### -param ipProtocol [in]

Protocol of the port to find by type <a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_protocol">NET_FW_IP_PROTOCOL</a>.

### -param openPort [out]

Reference to the returned <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a> object.

## -returns

<h3>C++</h3>
If the method succeeds, the return value is S_OK.

If the method fails, the return value is one of the following error codes.



<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="E_ACCESSDENIED"></a><a id="e_accessdenied"></a>E_ACCESSDENIED

</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<a id="E_INVALIDARG"></a><a id="e_invalidarg"></a>E_INVALIDARG

</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<a id="E_OUTOFMEMORY"></a><a id="e_outofmemory"></a>E_OUTOFMEMORY

</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<a id="E_POINTER"></a><a id="e_pointer"></a>E_POINTER

</td>
<td width="60%">
The method failed due to an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<a id="HRESULT_FROM_WIN32_ERROR_FILE_NOT_FOUND__"></a><a id="hresult_from_win32_error_file_not_found__"></a>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) 

</td>
<td width="60%">
The requested item does not exist.

</td>
</tr>
</table>
 

<h3>VB</h3>
Reference to the returned 
<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>
 object.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFwOpenPorts</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_protocol">NET_FW_IP_PROTOCOL</a>