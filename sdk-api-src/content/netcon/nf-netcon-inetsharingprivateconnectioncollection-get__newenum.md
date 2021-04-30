---
UID: NF:netcon.INetSharingPrivateConnectionCollection.get__NewEnum
title: INetSharingPrivateConnectionCollection::get__NewEnum (netcon.h)
description: The get__NewEnum method retrieves an enumerator for the private connections collection.
helpviewer_keywords: ["INetSharingPrivateConnectionCollection interface [ICS/ICF]","get__NewEnum method","INetSharingPrivateConnectionCollection.get__NewEnum","INetSharingPrivateConnectionCollection::get__NewEnum","_ics_inetsharingprivateconnectioncollection_get__newenum","get__NewEnum","get__NewEnum method [ICS/ICF]","get__NewEnum method [ICS/ICF]","INetSharingPrivateConnectionCollection interface","ics.inetsharingprivateconnectioncollection_get__newenum","netcon/INetSharingPrivateConnectionCollection::get__NewEnum"]
old-location: ics\inetsharingprivateconnectioncollection_get__newenum.htm
tech.root: ics
ms.assetid: 526da220-5999-4b84-b617-26edf23c15ab
ms.date: 12/05/2018
ms.keywords: INetSharingPrivateConnectionCollection interface [ICS/ICF],get__NewEnum method, INetSharingPrivateConnectionCollection.get__NewEnum, INetSharingPrivateConnectionCollection::get__NewEnum, _ics_inetsharingprivateconnectioncollection_get__newenum, get__NewEnum, get__NewEnum method [ICS/ICF], get__NewEnum method [ICS/ICF],INetSharingPrivateConnectionCollection interface, ics.inetsharingprivateconnectioncollection_get__newenum, netcon/INetSharingPrivateConnectionCollection::get__NewEnum
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
 - INetSharingPrivateConnectionCollection::get__NewEnum
 - netcon/INetSharingPrivateConnectionCollection::get__NewEnum
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
 - INetSharingPrivateConnectionCollection.get__NewEnum
---

# INetSharingPrivateConnectionCollection::get__NewEnum


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get__NewEnum</b> method retrieves an enumerator for the private connections collection.

## -parameters

### -param pVal [out]

Pointer to an interface pointer that receives a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for the collection.

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

<a href="/windows/desktop/api/netcon/nn-netcon-inetsharingprivateconnectioncollection">INetSharingPrivateConnectionCollection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>