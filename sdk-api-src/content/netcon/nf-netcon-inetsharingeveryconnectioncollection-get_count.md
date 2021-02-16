---
UID: NF:netcon.INetSharingEveryConnectionCollection.get_Count
title: INetSharingEveryConnectionCollection::get_Count (netcon.h)
description: The get__Count method retrieves the number of items in the connections collection.
helpviewer_keywords: ["INetSharingEveryConnectionCollection interface [ICS/ICF]","get_Count method","INetSharingEveryConnectionCollection.get_Count","INetSharingEveryConnectionCollection::get_Count","_ics_inetsharingeveryconnectioncollection_get_count","get_Count","get_Count method [ICS/ICF]","get_Count method [ICS/ICF]","INetSharingEveryConnectionCollection interface","ics.inetsharingeveryconnectioncollection_get_count","netcon/INetSharingEveryConnectionCollection::get_Count"]
old-location: ics\inetsharingeveryconnectioncollection_get_count.htm
tech.root: ics
ms.assetid: c387ab2c-7edd-4975-a735-d555dd7191cf
ms.date: 12/05/2018
ms.keywords: INetSharingEveryConnectionCollection interface [ICS/ICF],get_Count method, INetSharingEveryConnectionCollection.get_Count, INetSharingEveryConnectionCollection::get_Count, _ics_inetsharingeveryconnectioncollection_get_count, get_Count, get_Count method [ICS/ICF], get_Count method [ICS/ICF],INetSharingEveryConnectionCollection interface, ics.inetsharingeveryconnectioncollection_get_count, netcon/INetSharingEveryConnectionCollection::get_Count
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetSharingEveryConnectionCollection::get_Count
 - netcon/INetSharingEveryConnectionCollection::get_Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingEveryConnectionCollection.get_Count
---

# INetSharingEveryConnectionCollection::get_Count


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

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

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingeveryconnectioncollection">INetSharingEveryConnectionCollection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>