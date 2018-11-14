---
UID: NF:netcon.INetSharingManager.get_EnumEveryConnection
title: INetSharingManager::get_EnumEveryConnection
author: windows-sdk-content
description: The get_EnumEveryConnection method retrieves an enumeration interface for all the connections in the connection folder.
old-location: ics\inetsharingmanager_get_enumeveryconnection.htm
tech.root: ICS
ms.assetid: f200ffbf-3ce1-4c1b-b4c6-28a8784b5cb8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_EnumEveryConnection method, INetSharingManager.get_EnumEveryConnection, INetSharingManager::get_EnumEveryConnection, _ics_inetsharingmanager_get_enumeveryconnection, get_EnumEveryConnection, get_EnumEveryConnection method [ICS/ICF], get_EnumEveryConnection method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_enumeveryconnection, netcon/INetSharingManager::get_EnumEveryConnection
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
 - INetSharingManager.get_EnumEveryConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- netcon.h
: 
- INetSharingManager.get_EnumEveryConnection
: 
---

# INetSharingManager::get_EnumEveryConnection


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>get_EnumEveryConnection</b> method retrieves an enumeration interface for all the connections in the connection folder.


## -parameters




### -param ppColl

TBD




#### - ppEnum [out]

Pointer to a pointer that, on successful return, points to an 
<a href="https://msdn.microsoft.com/a53c15f0-c7f3-49ea-a85d-663ad4b12f6e">INetSharingEveryConnectionCollection</a> interface.


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
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/d3be8047-e0d5-44b7-97d9-536bc4aa11c5">IEnumNetSharingEveryConnection</a>



<a href="https://msdn.microsoft.com/a53c15f0-c7f3-49ea-a85d-663ad4b12f6e">INetSharingEveryConnectionCollection</a>



<a href="https://msdn.microsoft.com/e7009d13-89c2-4fd9-8f6c-dcdc67178598">INetSharingManager</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

