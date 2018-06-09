---
UID: NF:netcon.INetSharingConfiguration.DisableInternetFirewall
title: INetSharingConfiguration::DisableInternetFirewall
author: windows-sdk-content
description: The DisableInternetFirewall method disables Internet Connection Firewall on this connection.
old-location: ics\inetsharingconfiguration_disableinternetfirewall.htm
old-project: ICS
ms.assetid: f0157376-7533-4155-801c-3db82290655d
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: DisableInternetFirewall, DisableInternetFirewall method [ICS/ICF], DisableInternetFirewall method [ICS/ICF],INetSharingConfiguration interface, INetSharingConfiguration interface [ICS/ICF],DisableInternetFirewall method, INetSharingConfiguration.DisableInternetFirewall, INetSharingConfiguration::DisableInternetFirewall, _ics_inetsharingconfiguration_disableinternetfirewall, ics.inetsharingconfiguration_disableinternetfirewall, netcon/INetSharingConfiguration::DisableInternetFirewall
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingConfiguration.DisableInternetFirewall
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetSharingConfiguration::DisableInternetFirewall


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>DisableInternetFirewall</b> method disables Internet Connection Firewall on this connection.


## -parameters






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



Calling this method triggers the following notification:

%programname% is attempting to disable your Internet Connection Firewall. This  makes your computer more vulnerable to Internet security threats. Do you want to allow %programname% to disable Internet Connection Firewall?

This method returns successfully even if Internet Connection Firewall was not enabled on this connection.

Use the 
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a> interface for a particular connection.

<b>Windows XP with SP2:  </b>Calling this API will disable the firewall on the specified interface, regardless of whether the Windows Firewall is on.




## -see-also




<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a>



<a href="https://msdn.microsoft.com/9805f6bf-ee06-469f-9b2f-e48caa582d1a">INetSharingConfiguration::EnableInternetFirewall</a>



<a href="https://msdn.microsoft.com/85f6b76f-3c31-4669-a54f-30d12a82935e">INetSharingConfiguration::get_InternetFirewallEnabled</a>
 

 

