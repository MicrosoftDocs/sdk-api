---
UID: NF:netcon.INetSharingEveryConnectionCollection.get_Count
title: INetSharingEveryConnectionCollection::get_Count method
author: windows-driver-content
description: The get__Count method retrieves the number of items in the connections collection.
old-location: ics\inetsharingeveryconnectioncollection_get_count.htm
old-project: ICS
ms.assetid: c387ab2c-7edd-4975-a735-d555dd7191cf
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: INetSharingEveryConnectionCollection, INetSharingEveryConnectionCollection interface [ICS/ICF], get_Count method, INetSharingEveryConnectionCollection::get_Count, _ics_inetsharingeveryconnectioncollection_get_count, get_Count method [ICS/ICF], get_Count method [ICS/ICF], INetSharingEveryConnectionCollection interface, get_Count,INetSharingEveryConnectionCollection.get_Count, ics.inetsharingeveryconnectioncollection_get_count, netcon/INetSharingEveryConnectionCollection::get_Count
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
-	INetSharingEveryConnectionCollection.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# INetSharingEveryConnectionCollection::get_Count method


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The <b>get__Count</b> method retrieves the number of items in the connections collection.


## -parameters




### -param pVal [out]

Pointer to a long variable that, on successful return, receives the number of items in the connections collection.


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




<a href="https://msdn.microsoft.com/a53c15f0-c7f3-49ea-a85d-663ad4b12f6e">INetSharingEveryConnectionCollection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

