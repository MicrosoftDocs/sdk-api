---
UID: NF:tapi3if.ITLocationInfo.get_TollPrefixList
title: ITLocationInfo::get_TollPrefixList (tapi3if.h)
description: The get_TollPrefixList method gets the toll prefix list.
helpviewer_keywords: ["ITLocationInfo interface [TAPI 2.2]","get_TollPrefixList method","ITLocationInfo.get_TollPrefixList","ITLocationInfo::get_TollPrefixList","_tapi3_itlocationinfo_get_tollprefixlist","get_TollPrefixList","get_TollPrefixList method [TAPI 2.2]","get_TollPrefixList method [TAPI 2.2]","ITLocationInfo interface","tapi3.itlocationinfo_get_tollprefixlist","tapi3if/ITLocationInfo::get_TollPrefixList"]
old-location: tapi3\itlocationinfo_get_tollprefixlist.htm
tech.root: tapi3
ms.assetid: 45297e46-b1c8-45b0-bb16-8c5d5666bbd0
ms.date: 12/05/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_TollPrefixList method, ITLocationInfo.get_TollPrefixList, ITLocationInfo::get_TollPrefixList, _tapi3_itlocationinfo_get_tollprefixlist, get_TollPrefixList, get_TollPrefixList method [TAPI 2.2], get_TollPrefixList method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_tollprefixlist, tapi3if/ITLocationInfo::get_TollPrefixList
req.header: tapi3if.h
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
 - ITLocationInfo::get_TollPrefixList
 - tapi3if/ITLocationInfo::get_TollPrefixList
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
 - ITLocationInfo.get_TollPrefixList
---

# ITLocationInfo::get_TollPrefixList


## -description

The 
<b>get_TollPrefixList</b> method gets the toll prefix list.

## -parameters

### -param ppTollList [out]

Pointer to the <b>BSTR</b> containing a list of toll prefixes.

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
The <i>ppTollList</i> parameter is not a valid pointer.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppTollList</i> parameter.
			

The value that this method returns corresponds to the <b>dwTollPrefixListSize</b> and <b>dwTollPrefixListOffset</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>