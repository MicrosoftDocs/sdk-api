---
UID: NF:netcon.INetSharingManager.get_EnumPrivateConnections
title: INetSharingManager::get_EnumPrivateConnections (netcon.h)
description: The get_EnumPrivateConnections method retrieves an enumeration interface for privately-shared connections.
helpviewer_keywords: ["INetSharingManager interface [ICS/ICF]","get_EnumPrivateConnections method","INetSharingManager.get_EnumPrivateConnections","INetSharingManager::get_EnumPrivateConnections","_ics_inetsharingmanager_get_enumprivateconnections","get_EnumPrivateConnections","get_EnumPrivateConnections method [ICS/ICF]","get_EnumPrivateConnections method [ICS/ICF]","INetSharingManager interface","ics.inetsharingmanager_get_enumprivateconnections","netcon/INetSharingManager::get_EnumPrivateConnections"]
old-location: ics\inetsharingmanager_get_enumprivateconnections.htm
tech.root: ics
ms.assetid: cb770e91-0d85-4f67-b7a1-8cc6e89620eb
ms.date: 12/05/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_EnumPrivateConnections method, INetSharingManager.get_EnumPrivateConnections, INetSharingManager::get_EnumPrivateConnections, _ics_inetsharingmanager_get_enumprivateconnections, get_EnumPrivateConnections, get_EnumPrivateConnections method [ICS/ICF], get_EnumPrivateConnections method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_enumprivateconnections, netcon/INetSharingManager::get_EnumPrivateConnections
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
 - INetSharingManager::get_EnumPrivateConnections
 - netcon/INetSharingManager::get_EnumPrivateConnections
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
 - INetSharingManager.get_EnumPrivateConnections
---

# INetSharingManager::get_EnumPrivateConnections


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_EnumPrivateConnections</b> method retrieves an enumeration interface for privately-shared connections.

## -parameters

### -param Flags [in]

This parameter must be ICSSC_DEFAULT.

### -param ppColl [out]

Pointer to a pointer that, on successful return, points to an 
<a href="/windows/desktop/api/netcon/nn-netcon-inetsharingprivateconnectioncollection">INetSharingPrivateConnectionCollection</a> interface.

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

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-ienumnetsharingprivateconnection">IEnumNetSharingPrivateConnection</a>



<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager">INetSharingManager</a>



<a href="/windows/desktop/api/netcon/nn-netcon-inetsharingprivateconnectioncollection">INetSharingPrivateConnectionCollection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>