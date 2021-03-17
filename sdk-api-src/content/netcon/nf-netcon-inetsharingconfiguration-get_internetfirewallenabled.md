---
UID: NF:netcon.INetSharingConfiguration.get_InternetFirewallEnabled
title: INetSharingConfiguration::get_InternetFirewallEnabled (netcon.h)
description: The get_InternetFirewallEnabled method determines whether Internet Connection Firewall is enabled on this connection.
helpviewer_keywords: ["INetSharingConfiguration interface [ICS/ICF]","get_InternetFirewallEnabled method","INetSharingConfiguration.get_InternetFirewallEnabled","INetSharingConfiguration::get_InternetFirewallEnabled","_ics_inetsharingconfiguration_get_internetfirewallenabled","get_InternetFirewallEnabled","get_InternetFirewallEnabled method [ICS/ICF]","get_InternetFirewallEnabled method [ICS/ICF]","INetSharingConfiguration interface","ics.inetsharingconfiguration_get_internetfirewallenabled","netcon/INetSharingConfiguration::get_InternetFirewallEnabled"]
old-location: ics\inetsharingconfiguration_get_internetfirewallenabled.htm
tech.root: ics
ms.assetid: 85f6b76f-3c31-4669-a54f-30d12a82935e
ms.date: 12/05/2018
ms.keywords: INetSharingConfiguration interface [ICS/ICF],get_InternetFirewallEnabled method, INetSharingConfiguration.get_InternetFirewallEnabled, INetSharingConfiguration::get_InternetFirewallEnabled, _ics_inetsharingconfiguration_get_internetfirewallenabled, get_InternetFirewallEnabled, get_InternetFirewallEnabled method [ICS/ICF], get_InternetFirewallEnabled method [ICS/ICF],INetSharingConfiguration interface, ics.inetsharingconfiguration_get_internetfirewallenabled, netcon/INetSharingConfiguration::get_InternetFirewallEnabled
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
 - INetSharingConfiguration::get_InternetFirewallEnabled
 - netcon/INetSharingConfiguration::get_InternetFirewallEnabled
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
 - INetSharingConfiguration.get_InternetFirewallEnabled
---

# INetSharingConfiguration::get_InternetFirewallEnabled


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_InternetFirewallEnabled</b> method determines whether Internet Connection Firewall is enabled on this connection.

## -parameters

### -param pbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> variable that, on successful return, specifies whether Internet Connection Firewall is enabled. If Internet Connection Firewall is enabled, this value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

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
The operation was stopped.

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
One of the parameters is not valid.

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

Use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface for a particular connection.

<b>Windows XP with SP2:  </b> The resulting  firewall status is determined by the combination of  two levels: First check the global operation mode, then the mode on the interface of interest. Use the procedure <a href="/previous-versions/windows/desktop/ics/checking-the-effective-firewall-status">Checking the Effective Firewall Status</a> to determine the overall operational state.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a>



<a href="/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-disableinternetfirewall">INetSharingConfiguration::DisableInternetFirewall</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-enableinternetfirewall">INetSharingConfiguration::EnableInternetFirewall</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>