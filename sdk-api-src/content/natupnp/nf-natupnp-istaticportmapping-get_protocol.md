---
UID: NF:natupnp.IStaticPortMapping.get_Protocol
title: IStaticPortMapping::get_Protocol (natupnp.h)
description: The get_Protocol method retrieves the protocol associated with this port mapping.helpviewer_keywords: ["IStaticPortMapping interface [ICS/ICF]","get_Protocol method","IStaticPortMapping.get_Protocol","IStaticPortMapping::get_Protocol","_ics_istaticportmapping_get_protocol","get_Protocol","get_Protocol method [ICS/ICF]","get_Protocol method [ICS/ICF]","IStaticPortMapping interface","ics.istaticportmapping_get_protocol","natupnp/IStaticPortMapping::get_Protocol"]
old-location: ics\istaticportmapping_get_protocol.htm
tech.root: ics
ms.assetid: b9fc5ccc-43af-4dce-ba69-d11cdb4e3154
ms.date: 12/05/2018
ms.keywords: IStaticPortMapping interface [ICS/ICF],get_Protocol method, IStaticPortMapping.get_Protocol, IStaticPortMapping::get_Protocol, _ics_istaticportmapping_get_protocol, get_Protocol, get_Protocol method [ICS/ICF], get_Protocol method [ICS/ICF],IStaticPortMapping interface, ics.istaticportmapping_get_protocol, natupnp/IStaticPortMapping::get_Protocol
f1_keywords:
- natupnp/IStaticPortMapping.get_Protocol
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Hnetcfg.dll
api_name:
- IStaticPortMapping.get_Protocol
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStaticPortMapping::get_Protocol


## -description


The 
<b>get_Protocol</b> method retrieves the protocol associated with this port mapping.


## -parameters




### -param pVal [out]

Pointer to a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a> variable that, receives the protocol for this port mapping. The protocol is either "UDP" or "TCP".


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmapping">IStaticPortMapping</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>
 

 

