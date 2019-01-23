---
UID: NF:netcon.INetSharingConfiguration.DisableSharing
title: INetSharingConfiguration::DisableSharing
author: windows-sdk-content
description: The DisableSharing method disables sharing on this connection. It also disables all mappings on this connection. It does not disable Internet Connection Firewall or bridge configuration.
old-location: ics\inetsharingconfiguration_disablesharing.htm
tech.root: ics
ms.assetid: 85fda578-603c-4447-8546-374077235943
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DisableSharing, DisableSharing method [ICS/ICF], DisableSharing method [ICS/ICF],INetSharingConfiguration interface, INetSharingConfiguration interface [ICS/ICF],DisableSharing method, INetSharingConfiguration.DisableSharing, INetSharingConfiguration::DisableSharing, _ics_inetsharingconfiguration_disablesharing, ics.inetsharingconfiguration_disablesharing, netcon/INetSharingConfiguration::DisableSharing
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
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingConfiguration.DisableSharing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingConfiguration::DisableSharing


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/en-us/library/Aa366453(v=VS.85).aspx">Windows Firewall API</a>.]

The 
<b>DisableSharing</b> method disables sharing on this connection. It also disables all mappings on this connection. It does not disable Internet Connection Firewall or bridge configuration.


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

%programname% is attempting to disable Internet Connection Sharing (ICS). The following number of users or computers are currently sharing the Internet connection: %number%. Do you want to allow %programname% to disable ICS?

This method returns successfully when called on a connection that is not enabled for sharing. In this case, the method still disables all mappings on the connection.

Use the 
<a href="https://msdn.microsoft.com/en-us/library/Aa365966(v=VS.85).aspx">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://msdn.microsoft.com/en-us/library/Aa365935(v=VS.85).aspx">INetSharingConfiguration</a> interface for a particular connection.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa365935(v=VS.85).aspx">INetSharingConfiguration</a>



<a href="https://msdn.microsoft.com/40b2a2ff-50f4-484c-bf79-ae99a348644f">INetSharingConfiguration::EnableSharing</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa365952(v=VS.85).aspx">INetSharingConfiguration::get_SharingEnabled</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366131(v=VS.85).aspx">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

