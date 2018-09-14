---
UID: NF:netcon.INetSharingConfiguration.get_SharingEnabled
title: INetSharingConfiguration::get_SharingEnabled
author: windows-sdk-content
description: The get_SharingEnabled method determines whether sharing is enabled on this connection.
old-location: ics\inetsharingconfiguration_get_sharingenabled.htm
tech.root: ICS
ms.assetid: b8872235-0ef3-4ade-8085-fd90f40549af
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INetSharingConfiguration interface [ICS/ICF],get_SharingEnabled method, INetSharingConfiguration.get_SharingEnabled, INetSharingConfiguration::get_SharingEnabled, _ics_inetsharingconfiguration_get_sharingenabled, get_SharingEnabled, get_SharingEnabled method [ICS/ICF], get_SharingEnabled method [ICS/ICF],INetSharingConfiguration interface, ics.inetsharingconfiguration_get_sharingenabled, netcon/INetSharingConfiguration::get_SharingEnabled
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
 - INetSharingConfiguration.get_SharingEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingConfiguration::get_SharingEnabled


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>get_SharingEnabled</b> method determines whether sharing is enabled on this connection.


## -parameters




### -param pbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> variable that, on successful return, specifies whether sharing is enable on this connection. If sharing is enable, this value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.


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
<a href="https://msdn.microsoft.com/7cf705dd-41c3-4ac7-a75f-5677a7b49645">INetSharingManager::get_SharingInstalled</a>.

Use the 
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a> interface for a particular connection.




## -see-also




<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a>



<a href="https://msdn.microsoft.com/85fda578-603c-4447-8546-374077235943">INetSharingConfiguration::DisableSharing</a>



<a href="https://msdn.microsoft.com/40b2a2ff-50f4-484c-bf79-ae99a348644f">INetSharingConfiguration::EnableSharing</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="https://msdn.microsoft.com/97409190-55b3-412f-b654-e5b27928a4c3">SHARINGCONNECTIONTYPE</a>
 

 

