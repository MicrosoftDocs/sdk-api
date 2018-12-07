---
UID: NF:netcon.INetSharingManager.get_NetConnectionProps
title: INetSharingManager::get_NetConnectionProps
author: windows-sdk-content
description: The get_NetConnectionProps method retrieves a properties interface for the specified connection.
old-location: ics\inetsharingmanager_get_netconnectionprops.htm
tech.root: ics
ms.assetid: bf2db553-f324-4f23-b96e-f8ae703aa3ea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_NetConnectionProps method, INetSharingManager.get_NetConnectionProps, INetSharingManager::get_NetConnectionProps, _ics_inetsharingmanager_get_netconnectionprops, get_NetConnectionProps, get_NetConnectionProps method [ICS/ICF], get_NetConnectionProps method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_netconnectionprops, netcon/INetSharingManager::get_NetConnectionProps
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
 - INetSharingManager.get_NetConnectionProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingManager::get_NetConnectionProps


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>get_NetConnectionProps</b> method retrieves a properties interface for the specified connection.


## -parameters




### -param pNetConnection [in]

Pointer to an 
<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a> interface for the connection for which to retrieve the properties interface.


### -param ppProps [out]

Pointer to an interface pointer that, on successful return, points to an 
<a href="https://msdn.microsoft.com/8152f75c-1c93-4c30-8a13-c47fd5dde4af">INetConnectionProps</a> interface for the connection.


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



Not all connections can be configured for sharing. Retrieve the properties for the connection to verify that the connection can be shared before calling 
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a>.




## -see-also




<a href="https://msdn.microsoft.com/e7009d13-89c2-4fd9-8f6c-dcdc67178598">INetSharingManager</a>



<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

