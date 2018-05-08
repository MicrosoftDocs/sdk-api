---
UID: NF:netcon.INetSharingConfiguration.get_InternetFirewallEnabled
title: INetSharingConfiguration::get_InternetFirewallEnabled
author: windows-driver-content
description: The get_InternetFirewallEnabled method determines whether Internet Connection Firewall is enabled on this connection.
old-location: ics\inetsharingconfiguration_get_internetfirewallenabled.htm
old-project: ICS
ms.assetid: 85f6b76f-3c31-4669-a54f-30d12a82935e
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: INetSharingConfiguration interface [ICS/ICF],get_InternetFirewallEnabled method, INetSharingConfiguration.get_InternetFirewallEnabled, INetSharingConfiguration::get_InternetFirewallEnabled, _ics_inetsharingconfiguration_get_internetfirewallenabled, get_InternetFirewallEnabled, get_InternetFirewallEnabled method [ICS/ICF], get_InternetFirewallEnabled method [ICS/ICF],INetSharingConfiguration interface, ics.inetsharingconfiguration_get_internetfirewallenabled, netcon/INetSharingConfiguration::get_InternetFirewallEnabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Hnetcfg.dll
api_name:
-	INetSharingConfiguration.get_InternetFirewallEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetSharingConfiguration::get_InternetFirewallEnabled


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

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
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a> interface for a particular connection.

<b>Windows XP with SP2:  </b> The resulting  firewall status is determined by the combination of  two levels: First check the global operation mode, then the mode on the interface of interest. Use the procedure <a href="https://msdn.microsoft.com/c2a6f57d-e05b-4143-90ad-39ca32d66c66">Checking the Effective Firewall Status</a> to determine the overall operational state. 




## -see-also




<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a>



<a href="https://msdn.microsoft.com/f0157376-7533-4155-801c-3db82290655d">INetSharingConfiguration::DisableInternetFirewall</a>



<a href="https://msdn.microsoft.com/9805f6bf-ee06-469f-9b2f-e48caa582d1a">INetSharingConfiguration::EnableInternetFirewall</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

