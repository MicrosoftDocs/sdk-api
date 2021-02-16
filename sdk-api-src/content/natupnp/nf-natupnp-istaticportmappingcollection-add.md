---
UID: NF:natupnp.IStaticPortMappingCollection.Add
title: IStaticPortMappingCollection::Add (natupnp.h)
description: The Add method creates a new port mapping and adds it to the collection.
helpviewer_keywords: ["Add","Add method [ICS/ICF]","Add method [ICS/ICF]","IStaticPortMappingCollection interface","IStaticPortMappingCollection interface [ICS/ICF]","Add method","IStaticPortMappingCollection.Add","IStaticPortMappingCollection::Add","_ics_istaticportmappingcollection_add","ics.istaticportmappingcollection_add","natupnp/IStaticPortMappingCollection::Add"]
old-location: ics\istaticportmappingcollection_add.htm
tech.root: ics
ms.assetid: 5e61629d-80e4-4d44-8e53-12e17b399126
ms.date: 12/05/2018
ms.keywords: Add, Add method [ICS/ICF], Add method [ICS/ICF],IStaticPortMappingCollection interface, IStaticPortMappingCollection interface [ICS/ICF],Add method, IStaticPortMappingCollection.Add, IStaticPortMappingCollection::Add, _ics_istaticportmappingcollection_add, ics.istaticportmappingcollection_add, natupnp/IStaticPortMappingCollection::Add
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
 - IStaticPortMappingCollection::Add
 - natupnp/IStaticPortMappingCollection::Add
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
 - IStaticPortMappingCollection.Add
---

# IStaticPortMappingCollection::Add


## -description

The 
<b>Add</b> method creates a new port mapping and adds it to the collection.

## -parameters

### -param lExternalPort [in]

Specifies the external port for this port mapping.

### -param bstrProtocol [in]

Specifies the protocol. This parameter should be either UDP or TCP.

### -param lInternalPort [in]

Specifies the internal port for this port mapping.

### -param bstrInternalClient [in]

Specifies the name of the client on the private network that uses this port mapping.

### -param bEnabled [in]

Specifies whether the port is 
<a href="/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-enable">enabled</a>.

### -param bstrDescription [in]

Specifies a description for this port mapping.

### -param ppSPM [out]

Pointer to an interface pointer that, on successful return, receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmapping">IStaticPortMapping</a> interface.

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

## -remarks

The NAT API with UPnP technology uses the combination of the external port and the protocol to identify the port mapping.

## -see-also

<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmapping">IStaticPortMapping</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmappingcollection">IStaticPortMappingCollection</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmappingcollection-remove">IStaticPortMappingCollection::Remove</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>