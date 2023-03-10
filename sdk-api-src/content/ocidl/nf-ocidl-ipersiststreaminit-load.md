---
UID: NF:ocidl.IPersistStreamInit.Load
title: IPersistStreamInit::Load (ocidl.h)
description: Initializes an object from the stream where it was saved previously. (IPersistStreamInit.Load)
helpviewer_keywords: ["IPersistStreamInit interface [COM]","Load method","IPersistStreamInit.Load","IPersistStreamInit::Load","Load","Load method [COM]","Load method [COM]","IPersistStreamInit interface","_com_ipersiststreaminit_load","com.ipersiststreaminit_load","ocidl/IPersistStreamInit::Load"]
old-location: com\ipersiststreaminit_load.htm
tech.root: com
ms.assetid: 3e995e07-e088-40de-ba28-c30caea45786
ms.date: 12/05/2018
ms.keywords: IPersistStreamInit interface [COM],Load method, IPersistStreamInit.Load, IPersistStreamInit::Load, Load, Load method [COM], Load method [COM],IPersistStreamInit interface, _com_ipersiststreaminit_load, com.ipersiststreaminit_load, ocidl/IPersistStreamInit::Load
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistStreamInit::Load
 - ocidl/IPersistStreamInit::Load
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPersistStreamInit.Load
---

# IPersistStreamInit::Load


## -description

Initializes an object from the stream where it was saved previously.

## -parameters

### -param pStm [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer to the stream from which the object should be loaded.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to lack of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to some reason other than a lack of memory.

</td>
</tr>
</table>

## -remarks

If the object has already been initialized with <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew">IPersistStreamInit::InitNew</a>, then this method must return E_UNEXPECTED.

This method loads an object from its associated stream. The seek pointer is set as it was in the most recent <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-save">IPersistStreamInit::Save</a> method. This method can seek and read from the stream, but cannot write to it.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>
