---
UID: NF:natupnp.IStaticPortMappingCollection.get__NewEnum
title: IStaticPortMappingCollection::get__NewEnum (natupnp.h)
description: The get__NewEnum method retrieves an enumerator for the static port mappings collection.
helpviewer_keywords: ["IStaticPortMappingCollection interface [ICS/ICF]","get__NewEnum method","IStaticPortMappingCollection.get__NewEnum","IStaticPortMappingCollection::get__NewEnum","_ics_istaticportmappingcollection_get__newenum","get__NewEnum","get__NewEnum method [ICS/ICF]","get__NewEnum method [ICS/ICF]","IStaticPortMappingCollection interface","ics.istaticportmappingcollection_get__newenum","natupnp/IStaticPortMappingCollection::get__NewEnum"]
old-location: ics\istaticportmappingcollection_get__newenum.htm
tech.root: ics
ms.assetid: d1a2fa98-d1f2-404c-84fb-b3dccc60031f
ms.date: 12/05/2018
ms.keywords: IStaticPortMappingCollection interface [ICS/ICF],get__NewEnum method, IStaticPortMappingCollection.get__NewEnum, IStaticPortMappingCollection::get__NewEnum, _ics_istaticportmappingcollection_get__newenum, get__NewEnum, get__NewEnum method [ICS/ICF], get__NewEnum method [ICS/ICF],IStaticPortMappingCollection interface, ics.istaticportmappingcollection_get__newenum, natupnp/IStaticPortMappingCollection::get__NewEnum
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
 - IStaticPortMappingCollection::get__NewEnum
 - natupnp/IStaticPortMappingCollection::get__NewEnum
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
 - IStaticPortMappingCollection.get__NewEnum
---

# IStaticPortMappingCollection::get__NewEnum


## -description

The 
<b>get__NewEnum</b> method retrieves an enumerator for the static port mappings collection.

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

<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmappingcollection">IStaticPortMappingCollection</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>