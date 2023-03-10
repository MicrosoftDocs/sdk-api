---
UID: NF:tapi3.ITACDGroup.get_Name
title: ITACDGroup::get_Name (tapi3.h)
description: The ITACDGroup::get_Name method (tapi3.h) gets the ACD group name. This string can be a displayable name for the group.
helpviewer_keywords: ["ITACDGroup interface [TAPI 2.2]","get_Name method","ITACDGroup.get_Name","ITACDGroup::get_Name","_tapi3_itacdgroup_get_name","get_Name","get_Name method [TAPI 2.2]","get_Name method [TAPI 2.2]","ITACDGroup interface","tapi3.itacdgroup_get_name","tapi3cc/ITACDGroup::get_Name"]
old-location: tapi3\itacdgroup_get_name.htm
tech.root: tapi3
ms.assetid: 93e61a42-3e60-4d52-bb19-68842f6947da
ms.date: 08/09/2022
ms.keywords: ITACDGroup interface [TAPI 2.2],get_Name method, ITACDGroup.get_Name, ITACDGroup::get_Name, _tapi3_itacdgroup_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITACDGroup interface, tapi3.itacdgroup_get_name, tapi3cc/ITACDGroup::get_Name
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITACDGroup::get_Name
 - tapi3/ITACDGroup::get_Name
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITACDGroup.get_Name
---

# ITACDGroup::get_Name


## -description

The 
<b>get_Name</b> method gets the ACD group name. This string can be a displayable name for the group.

## -parameters

### -param ppName [out]

Pointer to <b>BSTR</b> representation of group name.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppName</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

The application must free <i>ppName</i> through 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when the variable is no longer needed.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>
