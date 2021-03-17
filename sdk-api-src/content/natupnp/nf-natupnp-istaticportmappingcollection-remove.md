---
UID: NF:natupnp.IStaticPortMappingCollection.Remove
title: IStaticPortMappingCollection::Remove (natupnp.h)
description: The Remove method removes the specified port mapping from the collection.
helpviewer_keywords: ["IStaticPortMappingCollection interface [ICS/ICF]","Remove method","IStaticPortMappingCollection.Remove","IStaticPortMappingCollection::Remove","Remove","Remove method [ICS/ICF]","Remove method [ICS/ICF]","IStaticPortMappingCollection interface","_ics_istaticportmappingcollection_remove","ics.istaticportmappingcollection_remove","natupnp/IStaticPortMappingCollection::Remove"]
old-location: ics\istaticportmappingcollection_remove.htm
tech.root: ics
ms.assetid: c82a145d-7b85-419b-b64b-36f1ac7a2631
ms.date: 12/05/2018
ms.keywords: IStaticPortMappingCollection interface [ICS/ICF],Remove method, IStaticPortMappingCollection.Remove, IStaticPortMappingCollection::Remove, Remove, Remove method [ICS/ICF], Remove method [ICS/ICF],IStaticPortMappingCollection interface, _ics_istaticportmappingcollection_remove, ics.istaticportmappingcollection_remove, natupnp/IStaticPortMappingCollection::Remove
req.header: natupnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IStaticPortMappingCollection::Remove
 - natupnp/IStaticPortMappingCollection::Remove
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
 - IStaticPortMappingCollection.Remove
---

# IStaticPortMappingCollection::Remove


## -description

The 
<b>Remove</b> method removes the specified port mapping from the collection.

## -parameters

### -param lExternalPort [in]

Specifies the external port for this port mapping.

### -param bstrProtocol [in]

Specifies the protocol. This parameter should be either UDP or TCP.

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

The NAT API with UPnP technology uses the combination of the external port and the protocol to identify the port mapping.

## -see-also

<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmapping">IStaticPortMapping</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmappingcollection">IStaticPortMappingCollection</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmappingcollection-add">IStaticPortMappingCollection::Add</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>