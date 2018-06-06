---
UID: NF:netcon.INetSharingManager.get_EnumPublicConnections
title: INetSharingManager::get_EnumPublicConnections
author: windows-sdk-content
description: The EnumPublicConnections method retrieves an enumeration interface for publicly-shared connections.
old-location: ics\inetsharingmanager_get_enumpublicconnections.htm
old-project: ICS
ms.assetid: 7db0eb73-8e0f-4267-9a88-20952f3721e2
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_EnumPublicConnections method, INetSharingManager.get_EnumPublicConnections, INetSharingManager::get_EnumPublicConnections, _ics_inetsharingmanager_get_enumpublicconnections, get_EnumPublicConnections, get_EnumPublicConnections method [ICS/ICF], get_EnumPublicConnections method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_enumpublicconnections, netcon/INetSharingManager::get_EnumPublicConnections
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
 - INetSharingManager.get_EnumPublicConnections
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetSharingManager::get_EnumPublicConnections


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The <b>EnumPublicConnections</b> method retrieves an enumeration interface for publicly-shared connections.


## -parameters




### -param Flags [in]

This parameter must be ICSSC_DEFAULT.


### -param ppColl






#### - ppEnum [out]

Pointer to a pointer that, on successful return, points to an 
<a href="https://msdn.microsoft.com/92027ba2-b803-4c9f-ae77-a89074fef718">INetSharingPublicConnectionCollection</a> interface.


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




<a href="https://msdn.microsoft.com/69f2d4c0-7c25-4a50-988b-3ca6babb489a">IEnumNetSharingPublicConnection</a>



<a href="https://msdn.microsoft.com/e7009d13-89c2-4fd9-8f6c-dcdc67178598">INetSharingManager</a>



<a href="https://msdn.microsoft.com/92027ba2-b803-4c9f-ae77-a89074fef718">INetSharingPublicConnectionCollection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

