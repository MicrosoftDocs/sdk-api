---
UID: NF:natupnp.IStaticPortMappingCollection.get_Count
title: IStaticPortMappingCollection::get_Count (natupnp.h)
description: The get_Count method retrieves the number of port mappings in the collection.
helpviewer_keywords: ["IStaticPortMappingCollection interface [ICS/ICF]","get_Count method","IStaticPortMappingCollection.get_Count","IStaticPortMappingCollection::get_Count","_ics_istaticportmappingcollection_get_count","get_Count","get_Count method [ICS/ICF]","get_Count method [ICS/ICF]","IStaticPortMappingCollection interface","ics.istaticportmappingcollection_get_count","natupnp/IStaticPortMappingCollection::get_Count"]
old-location: ics\istaticportmappingcollection_get_count.htm
tech.root: ics
ms.assetid: 8ececd98-a700-4d64-8f89-a1ec36597edf
ms.date: 12/05/2018
ms.keywords: IStaticPortMappingCollection interface [ICS/ICF],get_Count method, IStaticPortMappingCollection.get_Count, IStaticPortMappingCollection::get_Count, _ics_istaticportmappingcollection_get_count, get_Count, get_Count method [ICS/ICF], get_Count method [ICS/ICF],IStaticPortMappingCollection interface, ics.istaticportmappingcollection_get_count, natupnp/IStaticPortMappingCollection::get_Count
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
 - IStaticPortMappingCollection::get_Count
 - natupnp/IStaticPortMappingCollection::get_Count
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
 - IStaticPortMappingCollection.get_Count
---

# IStaticPortMappingCollection::get_Count


## -description

The 
<b>get_Count</b> method retrieves the number of port mappings in the collection.

## -parameters

### -param pVal [out]

Pointer to a <b>long</b> variable that receives the number of port mappings in the collection.

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

<a href="/previous-versions/windows/desktop/api/natupnp/nf-natupnp-inatnumberofentriescallback-newnumberofentries">INATNumberOfEntriesCallback::NewNumberOfEntries</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmappingcollection">IStaticPortMappingCollection</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>