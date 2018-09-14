---
UID: NF:netcon.INetSharingPublicConnectionCollection.get__NewEnum
title: INetSharingPublicConnectionCollection::get__NewEnum
author: windows-sdk-content
description: The get__NewEnum method retrieves an enumerator for the public connections collection.
old-location: ics\inetsharingpublicconnectioncollection_get__newenum.htm
tech.root: ICS
ms.assetid: 169de955-d53d-410e-b2e6-911ab0a78bba
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INetSharingPublicConnectionCollection interface [ICS/ICF],get__NewEnum method, INetSharingPublicConnectionCollection.get__NewEnum, INetSharingPublicConnectionCollection::get__NewEnum, _ics_inetsharingpublicconnectioncollection_get__newenum, get__NewEnum, get__NewEnum method [ICS/ICF], get__NewEnum method [ICS/ICF],INetSharingPublicConnectionCollection interface, ics.inetsharingpublicconnectioncollection_get__newenum, netcon/INetSharingPublicConnectionCollection::get__NewEnum
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
 - INetSharingPublicConnectionCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingPublicConnectionCollection::get__NewEnum


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>get__NewEnum</b> method retrieves an enumerator for the public connections collection.


## -parameters




### -param pVal [out]

Pointer to an interface pointer that receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface for the collection.


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




<a href="https://msdn.microsoft.com/92027ba2-b803-4c9f-ae77-a89074fef718">INetSharingPublicConnectionCollection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

