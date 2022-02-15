---
UID: NF:vss.IVssEnumObject.Reset
title: IVssEnumObject::Reset (vss.h)
description: Resets the enumerator so that IVssEnumObject:Next starts at the first enumerated object.
helpviewer_keywords: ["IVssEnumObject interface [VSS]","Reset method","IVssEnumObject.Reset","IVssEnumObject::Reset","Reset","Reset method [VSS]","Reset method [VSS]","IVssEnumObject interface","_win32_ivssenumobject_reset","base.ivssenumobject_reset","vss/IVssEnumObject::Reset"]
old-location: base\ivssenumobject_reset.htm
tech.root: base
ms.assetid: 98fc07b0-3efe-4ec3-bb70-64a8b8828162
ms.date: 12/05/2018
ms.keywords: IVssEnumObject interface [VSS],Reset method, IVssEnumObject.Reset, IVssEnumObject::Reset, Reset, Reset method [VSS], Reset method [VSS],IVssEnumObject interface, _win32_ivssenumobject_reset, base.ivssenumobject_reset, vss/IVssEnumObject::Reset
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
 - IVssEnumObject::Reset
 - vss/IVssEnumObject::Reset
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
 - IVssEnumObject.Reset
---

# IVssEnumObject::Reset


## -description

The <b>Reset</b> method resets the enumerator 
    so that <a href="/windows/desktop/api/vss/nf-vss-ivssenumobject-next">IVssEnumObject:Next</a> starts at the first 
    enumerated object.



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



<a href="/windows/desktop/api/vss/nf-vss-ivssenumobject-next">IVssEnumObject:Next</a>
