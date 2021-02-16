---
UID: NF:natupnp.IStaticPortMapping.Enable
title: IStaticPortMapping::Enable (natupnp.h)
description: The Enable method enables or disables this port mapping.
helpviewer_keywords: ["Enable","Enable method [ICS/ICF]","Enable method [ICS/ICF]","IStaticPortMapping interface","IStaticPortMapping interface [ICS/ICF]","Enable method","IStaticPortMapping.Enable","IStaticPortMapping::Enable","_ics_istaticportmapping_enable","ics.istaticportmapping_enable","natupnp/IStaticPortMapping::Enable"]
old-location: ics\istaticportmapping_enable.htm
tech.root: ics
ms.assetid: 66aa27b4-83a5-4c20-b964-084dd0e48a54
ms.date: 12/05/2018
ms.keywords: Enable, Enable method [ICS/ICF], Enable method [ICS/ICF],IStaticPortMapping interface, IStaticPortMapping interface [ICS/ICF],Enable method, IStaticPortMapping.Enable, IStaticPortMapping::Enable, _ics_istaticportmapping_enable, ics.istaticportmapping_enable, natupnp/IStaticPortMapping::Enable
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
 - IStaticPortMapping::Enable
 - natupnp/IStaticPortMapping::Enable
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
 - IStaticPortMapping.Enable
---

# IStaticPortMapping::Enable


## -description

The 
<b>Enable</b> method enables or disables this port mapping.

## -parameters

### -param vb [in]

Specifies a value that indicates whether the port mapping should be enabled or disabled. To enable the port mapping specify VARIANT_TRUE. To disable the port mapping specify VARIANT_FALSE.

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

<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmapping">IStaticPortMapping</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_enabled">IStaticPortMapping::get_InternalEnabled</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>