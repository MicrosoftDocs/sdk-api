---
UID: NF:netcon.INetSharingConfiguration.EnableSharing
title: INetSharingConfiguration::EnableSharing (netcon.h)
description: The EnableSharing method enables sharing on this connection.
helpviewer_keywords: ["EnableSharing","EnableSharing method [ICS/ICF]","EnableSharing method [ICS/ICF]","INetSharingConfiguration interface","INetSharingConfiguration interface [ICS/ICF]","EnableSharing method","INetSharingConfiguration.EnableSharing","INetSharingConfiguration::EnableSharing","_ics_inetsharingconfiguration_enablesharing","ics.inetsharingconfiguration_enablesharing","netcon/INetSharingConfiguration::EnableSharing"]
old-location: ics\inetsharingconfiguration_enablesharing.htm
tech.root: ics
ms.assetid: 40b2a2ff-50f4-484c-bf79-ae99a348644f
ms.date: 12/05/2018
ms.keywords: EnableSharing, EnableSharing method [ICS/ICF], EnableSharing method [ICS/ICF],INetSharingConfiguration interface, INetSharingConfiguration interface [ICS/ICF],EnableSharing method, INetSharingConfiguration.EnableSharing, INetSharingConfiguration::EnableSharing, _ics_inetsharingconfiguration_enablesharing, ics.inetsharingconfiguration_enablesharing, netcon/INetSharingConfiguration::EnableSharing
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
 - INetSharingConfiguration::EnableSharing
 - netcon/INetSharingConfiguration::EnableSharing
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
 - INetSharingConfiguration.EnableSharing
---

# INetSharingConfiguration::EnableSharing


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>EnableSharing</b> method enables sharing on this connection.

## -parameters

### -param Type [in]

Specifies whether this connection is shared publicly or privately.

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

Calling this method triggers the following notification:

%programname% is attempting to enable Internet Connection Sharing on the network connection %connectionname%. This will allow other computers on your network to connect to the Internet through a shared public connection. Do you want %programname% to enable Internet Connection Sharing on this connection?

If the calling application specifies that this connection is publicly shared, any previous publicly-shared connection is automatically disabled.

A publicly-shared connection automatically has Internet Connection Firewall enabled. Privately-shared connections retain their existing settings.

Use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface for a particular connection.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing">INetSharingConfiguration::DisableSharing</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_sharingenabled">INetSharingConfiguration::get_SharingEnabled</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="/windows/desktop/api/netcon/ne-netcon-sharingconnectiontype">SHARINGCONNECTIONTYPE</a>