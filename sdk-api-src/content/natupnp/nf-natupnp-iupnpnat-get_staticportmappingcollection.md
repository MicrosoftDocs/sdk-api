---
UID: NF:natupnp.IUPnPNAT.get_StaticPortMappingCollection
title: IUPnPNAT::get_StaticPortMappingCollection (natupnp.h)
description: The get_StaticPortMappingCollection method retrieves an interface for the collection of static port mappings on the NAT used by the local computer.
helpviewer_keywords: ["IUPnPNAT interface [ICS/ICF]","get_StaticPortMappingCollection method","IUPnPNAT.get_StaticPortMappingCollection","IUPnPNAT::get_StaticPortMappingCollection","_ics_iupnpnat_get_staticportmappingcollection","get_StaticPortMappingCollection","get_StaticPortMappingCollection method [ICS/ICF]","get_StaticPortMappingCollection method [ICS/ICF]","IUPnPNAT interface","ics.iupnpnat_get_staticportmappingcollection","natupnp/IUPnPNAT::get_StaticPortMappingCollection"]
old-location: ics\iupnpnat_get_staticportmappingcollection.htm
tech.root: ics
ms.assetid: ba4d0735-f04e-47d1-a54c-e01cf338d737
ms.date: 12/05/2018
ms.keywords: IUPnPNAT interface [ICS/ICF],get_StaticPortMappingCollection method, IUPnPNAT.get_StaticPortMappingCollection, IUPnPNAT::get_StaticPortMappingCollection, _ics_iupnpnat_get_staticportmappingcollection, get_StaticPortMappingCollection, get_StaticPortMappingCollection method [ICS/ICF], get_StaticPortMappingCollection method [ICS/ICF],IUPnPNAT interface, ics.iupnpnat_get_staticportmappingcollection, natupnp/IUPnPNAT::get_StaticPortMappingCollection
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
 - IUPnPNAT::get_StaticPortMappingCollection
 - natupnp/IUPnPNAT::get_StaticPortMappingCollection
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
 - IUPnPNAT.get_StaticPortMappingCollection
---

# IUPnPNAT::get_StaticPortMappingCollection


## -description

The 
<b>get_StaticPortMappingCollection</b> method retrieves an interface for the collection of static port mappings on the NAT used by the local computer.

## -parameters

### -param ppSPMs [out]

Pointer to an interface pointer that points to an 
<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmappingcollection">IStaticPortMappingCollection</a> interface.

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

<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmappingcollection">IStaticPortMappingCollection</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-iupnpnat">IUPnPNAT</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>