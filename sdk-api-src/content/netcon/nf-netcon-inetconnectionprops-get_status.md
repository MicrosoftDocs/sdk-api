---
UID: NF:netcon.INetConnectionProps.get_Status
title: INetConnectionProps::get_Status (netcon.h)
description: The get_Status method retrieves the status of the connection.
helpviewer_keywords: ["INetConnectionProps interface [ICS/ICF]","get_Status method","INetConnectionProps.get_Status","INetConnectionProps::get_Status","_ics_inetconnectionprops_get_status","get_Status","get_Status method [ICS/ICF]","get_Status method [ICS/ICF]","INetConnectionProps interface","ics.inetconnectionprops_get_status","netcon/INetConnectionProps::get_Status"]
old-location: ics\inetconnectionprops_get_status.htm
tech.root: ics
ms.assetid: a8d9506a-00a4-4202-aa1f-652a71cb5f0a
ms.date: 12/05/2018
ms.keywords: INetConnectionProps interface [ICS/ICF],get_Status method, INetConnectionProps.get_Status, INetConnectionProps::get_Status, _ics_inetconnectionprops_get_status, get_Status, get_Status method [ICS/ICF], get_Status method [ICS/ICF],INetConnectionProps interface, ics.inetconnectionprops_get_status, netcon/INetConnectionProps::get_Status
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Hnetcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetConnectionProps::get_Status
 - netcon/INetConnectionProps::get_Status
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetConnectionProps.get_Status
---

# INetConnectionProps::get_Status


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_Status</b> method retrieves the status of the connection.

## -parameters

### -param pStatus [out]

Pointer to a variable of type 
<a href="/windows/desktop/api/netcon/ne-netcon-netcon_status">NETCON_STATUS</a> that, on successful return, receives a code that specifies the status of the connection.

## -returns

If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnectionprops">INetConnectionProps</a>



<a href="/windows/desktop/api/netcon/ne-netcon-netcon_status">NETCON_STATUS</a>