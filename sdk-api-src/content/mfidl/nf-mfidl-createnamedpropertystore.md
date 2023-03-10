---
UID: NF:mfidl.CreateNamedPropertyStore
title: CreateNamedPropertyStore function (mfidl.h)
description: Creates an empty property store to hold name/value pairs.
helpviewer_keywords: ["21f12bc1-606a-4ce8-bc8d-608d4d7cfc46","CreateNamedPropertyStore","CreateNamedPropertyStore function [Media Foundation]","mf.createnamedpropertystore","mfidl/CreateNamedPropertyStore"]
old-location: mf\createnamedpropertystore.htm
tech.root: mf
ms.assetid: 21f12bc1-606a-4ce8-bc8d-608d4d7cfc46
ms.date: 12/05/2018
ms.keywords: 21f12bc1-606a-4ce8-bc8d-608d4d7cfc46, CreateNamedPropertyStore, CreateNamedPropertyStore function [Media Foundation], mf.createnamedpropertystore, mfidl/CreateNamedPropertyStore
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateNamedPropertyStore
 - mfidl/CreateNamedPropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - CreateNamedPropertyStore
---

# CreateNamedPropertyStore function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Instead, applications should use the <b>PSCreateMemoryPropertyStore</b> function to create named property stores.]

Creates an empty property store to hold name/value pairs.

## -parameters

### -param ppStore [out]

Receives a pointer to the <b>INamedPropertyStore</b> interface. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>