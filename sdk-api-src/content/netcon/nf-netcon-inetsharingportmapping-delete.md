---
UID: NF:netcon.INetSharingPortMapping.Delete
title: INetSharingPortMapping::Delete
author: windows-sdk-content
description: The Delete method deletes a port mapping from the list of port mappings for a particular connection.
old-location: ics\inetsharingportmapping_delete.htm
tech.root: ICS
ms.assetid: f9582110-a717-41a4-8ddd-26ef703b8356
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Delete, Delete method [ICS/ICF], Delete method [ICS/ICF],INetSharingPortMapping interface, INetSharingPortMapping interface [ICS/ICF],Delete method, INetSharingPortMapping.Delete, INetSharingPortMapping::Delete, _ics_inetsharingportmapping_delete, ics.inetsharingportmapping_delete, netcon/INetSharingPortMapping::Delete
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
 - INetSharingPortMapping.Delete
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
- INetSharingPortMapping.Delete
: 
---

# INetSharingPortMapping::Delete


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>Delete</b> method deletes a port mapping from the list of port mappings for a particular connection.


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



Calling this method also removes the name of this port mapping from the list of mappings in the ICS/ICF user interface.




## -see-also




<a href="https://msdn.microsoft.com/2790aced-a3a9-425d-9e0f-fe8df4fcb934">INetSharingConfiguration::RemovePortMapping</a>



<a href="https://msdn.microsoft.com/236608c3-061e-4db0-96df-25d263b6463b">INetSharingPortMapping</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

