---
UID: NF:netcon.INetConnection.GetProperties
title: INetConnection::GetProperties (netcon.h)
description: The GetProperties method retrieves a structure that contains the properties for this network connection.
helpviewer_keywords: ["GetProperties","GetProperties method [ICS/ICF]","GetProperties method [ICS/ICF]","INetConnection interface","INetConnection interface [ICS/ICF]","GetProperties method","INetConnection.GetProperties","INetConnection::GetProperties","_ics_inetconnection_getproperties","ics.inetconnection_getproperties","netcon/INetConnection::GetProperties"]
old-location: ics\inetconnection_getproperties.htm
tech.root: ics
ms.assetid: ab27a7fd-061f-4ea2-8ce8-23d59957a46f
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [ICS/ICF], GetProperties method [ICS/ICF],INetConnection interface, INetConnection interface [ICS/ICF],GetProperties method, INetConnection.GetProperties, INetConnection::GetProperties, _ics_inetconnection_getproperties, ics.inetconnection_getproperties, netcon/INetConnection::GetProperties
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
 - INetConnection::GetProperties
 - netcon/INetConnection::GetProperties
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
 - INetConnection.GetProperties
---

# INetConnection::GetProperties


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>GetProperties</b> method retrieves a structure that contains the properties for this network connection.

## -parameters

### -param ppProps [out]

Pointer to a pointer that, on successful return, points to a 
<a href="/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a> structure that contains the properties for this network connection.

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

## -remarks

The calling application should free the memory occupied by the 
<a href="/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a> structure returned by <b>GetProperties</b>. Free the memory by calling the <a href="/windows/desktop/api/netcon/nf-netcon-ncfreenetconproperties">NcFreeNetconProperties</a> function. This function is defined in NetCon.h and is exported by NetShell.dll.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>