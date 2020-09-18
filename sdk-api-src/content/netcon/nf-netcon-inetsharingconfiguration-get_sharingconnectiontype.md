---
UID: NF:netcon.INetSharingConfiguration.get_SharingConnectionType
title: INetSharingConfiguration::get_SharingConnectionType (netcon.h)
description: The get_SharingConnectionType method determines the type of sharing that is enabled on this connection.
helpviewer_keywords: ["INetSharingConfiguration interface [ICS/ICF]","get_SharingConnectionType method","INetSharingConfiguration.get_SharingConnectionType","INetSharingConfiguration::get_SharingConnectionType","_ics_inetsharingconfiguration_get_sharingconnectiontype","get_SharingConnectionType","get_SharingConnectionType method [ICS/ICF]","get_SharingConnectionType method [ICS/ICF]","INetSharingConfiguration interface","ics.inetsharingconfiguration_get_sharingconnectiontype","netcon/INetSharingConfiguration::get_SharingConnectionType"]
old-location: ics\inetsharingconfiguration_get_sharingconnectiontype.htm
tech.root: ics
ms.assetid: 29dfc1cf-4b72-4ba8-9a5c-7e7dd20393ee
ms.date: 12/05/2018
ms.keywords: INetSharingConfiguration interface [ICS/ICF],get_SharingConnectionType method, INetSharingConfiguration.get_SharingConnectionType, INetSharingConfiguration::get_SharingConnectionType, _ics_inetsharingconfiguration_get_sharingconnectiontype, get_SharingConnectionType, get_SharingConnectionType method [ICS/ICF], get_SharingConnectionType method [ICS/ICF],INetSharingConfiguration interface, ics.inetsharingconfiguration_get_sharingconnectiontype, netcon/INetSharingConfiguration::get_SharingConnectionType
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
 - INetSharingConfiguration::get_SharingConnectionType
 - netcon/INetSharingConfiguration::get_SharingConnectionType
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
 - INetSharingConfiguration.get_SharingConnectionType
---

# INetSharingConfiguration::get_SharingConnectionType


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_SharingConnectionType</b> method determines the type of sharing that is enabled on this connection.

## -parameters

### -param pType [out]

Pointer to a variable of type 
<a href="/windows/desktop/api/netcon/ne-netcon-sharingconnectiontype">SHARINGCONNECTIONTYPE</a> that specifies whether this connection is shared publicly or privately.

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

To determine whether connection sharing is supported on the currently-installed operating system, use 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled">INetSharingManager::get_SharingInstalled</a>.

Use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface for a particular connection.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing">INetSharingConfiguration::DisableSharing</a>



<a href="/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing">INetSharingConfiguration::EnableSharing</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="/windows/desktop/api/netcon/ne-netcon-sharingconnectiontype">SHARINGCONNECTIONTYPE</a>