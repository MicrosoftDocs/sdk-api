---
UID: NF:vswriter.CreateVssExpressWriter
title: CreateVssExpressWriter function (vswriter.h)
description: The CreateVssExpressWriter function (vswriter.h) creates an IVssExpressWriter interface object and returns a pointer to it.
helpviewer_keywords: ["CreateVssExpressWriter","CreateVssExpressWriter function","CreateVssExpressWriterInternal","base.createvssexpresswriter","vswriter/CreateVssExpressWriter","vswriter/CreateVssExpressWriterInternal"]
old-location: base\createvssexpresswriter.htm
tech.root: base
ms.assetid: c24a1046-50b0-4fec-88f9-3bbd6970982a
ms.date: 08/09/2022
ms.keywords: CreateVssExpressWriter, CreateVssExpressWriter function, CreateVssExpressWriterInternal, base.createvssexpresswriter, vswriter/CreateVssExpressWriter, vswriter/CreateVssExpressWriterInternal
req.header: vswriter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateVssExpressWriter
 - vswriter/CreateVssExpressWriter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VssApi.dll
api_name:
 - CreateVssExpressWriter
 - CreateVssExpressWriterInternal
---

# CreateVssExpressWriter function


## -description

Creates an <a href="/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a> interface object and returns a pointer to it.<div class="alert"><b>Note</b>  This function is exported as <b>CreateVssExpressWriterInternal</b>, but you should call <b>CreateVssExpressWriter</b>, not <b>CreateVssExpressWriterInternal</b>.</div>
<div> </div>

## -parameters

### -param ppWriter [out]

Doubly indirect pointer to the newly created <a href="/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a> object.

## -returns

The return values listed here are in addition to the normal COM HRESULT values that may be returned at any time from the function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned a pointer to an 
        <a href="/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
</table>
