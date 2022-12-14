---
UID: NF:vss.IVssEnumObject.Skip
title: IVssEnumObject::Skip (vss.h)
description: Skips the specified number of objects. (IVssEnumObject.Skip)
helpviewer_keywords: ["IVssEnumObject interface [VSS]","Skip method","IVssEnumObject.Skip","IVssEnumObject::Skip","Skip","Skip method [VSS]","Skip method [VSS]","IVssEnumObject interface","_win32_ivssenumobject_skip","base.ivssenumobject_skip","vss/IVssEnumObject::Skip"]
old-location: base\ivssenumobject_skip.htm
tech.root: base
ms.assetid: a655978e-49fa-445d-8576-ba82b523750c
ms.date: 12/05/2018
ms.keywords: IVssEnumObject interface [VSS],Skip method, IVssEnumObject.Skip, IVssEnumObject::Skip, Skip, Skip method [VSS], Skip method [VSS],IVssEnumObject interface, _win32_ivssenumobject_skip, base.ivssenumobject_skip, vss/IVssEnumObject::Skip
req.header: vss.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssEnumObject::Skip
 - vss/IVssEnumObject::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssEnumObject.Skip
---

# IVssEnumObject::Skip


## -description

The <b>Skip</b> method skips the specified 
    number of objects.

## -parameters

### -param celt [in]

Number of elements to be skipped in the list of enumerated objects.

## -returns

The following are the valid return codes for this method.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to access a location beyond the end of the list of items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an internal error in the enumerator.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssenumobject">IVssEnumObject</a>
