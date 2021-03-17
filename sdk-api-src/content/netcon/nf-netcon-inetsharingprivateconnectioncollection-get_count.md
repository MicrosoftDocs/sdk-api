---
UID: NF:netcon.INetSharingPrivateConnectionCollection.get_Count
title: INetSharingPrivateConnectionCollection::get_Count (netcon.h)
description: The get__Count method retrieves the number of items in the private connections collection.
helpviewer_keywords: ["INetSharingPrivateConnectionCollection interface [ICS/ICF]","get_Count method","INetSharingPrivateConnectionCollection.get_Count","INetSharingPrivateConnectionCollection::get_Count","_ics_inetsharingprivateconnectioncollection_get_count","get_Count","get_Count method [ICS/ICF]","get_Count method [ICS/ICF]","INetSharingPrivateConnectionCollection interface","ics.inetsharingprivateconnectioncollection_get_count","netcon/INetSharingPrivateConnectionCollection::get_Count"]
old-location: ics\inetsharingprivateconnectioncollection_get_count.htm
tech.root: ics
ms.assetid: 599ffa10-6932-48bd-a736-60512f25271c
ms.date: 12/05/2018
ms.keywords: INetSharingPrivateConnectionCollection interface [ICS/ICF],get_Count method, INetSharingPrivateConnectionCollection.get_Count, INetSharingPrivateConnectionCollection::get_Count, _ics_inetsharingprivateconnectioncollection_get_count, get_Count, get_Count method [ICS/ICF], get_Count method [ICS/ICF],INetSharingPrivateConnectionCollection interface, ics.inetsharingprivateconnectioncollection_get_count, netcon/INetSharingPrivateConnectionCollection::get_Count
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
 - INetSharingPrivateConnectionCollection::get_Count
 - netcon/INetSharingPrivateConnectionCollection::get_Count
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
 - INetSharingPrivateConnectionCollection.get_Count
---

# INetSharingPrivateConnectionCollection::get_Count


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The <b>get__Count</b> method retrieves the number of items in the private connections collection.

## -parameters

### -param pVal [out]

Pointer to a <b>long</b> variable that receives the number of items in the private connections collection.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

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

<a href="/windows/desktop/api/netcon/nn-netcon-inetsharingprivateconnectioncollection">INetSharingPrivateConnectionCollection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>