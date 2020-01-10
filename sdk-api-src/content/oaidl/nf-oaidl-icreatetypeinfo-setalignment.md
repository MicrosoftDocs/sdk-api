---
UID: NF:oaidl.ICreateTypeInfo.SetAlignment
title: ICreateTypeInfo::SetAlignment (oaidl.h)
description: Specifies the data alignment for an item of TYPEKIND=TKIND_RECORD.
old-location: automat\icreatetypeinfo_setalignment.htm
tech.root: automat
ms.assetid: db21ab80-ea2f-4f9e-a43c-0d202e235516
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetAlignment method, ICreateTypeInfo.SetAlignment, ICreateTypeInfo::SetAlignment, SetAlignment, SetAlignment method [Automation], SetAlignment method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetAlignment, automat.icreatetypeinfo_setalignment, oaidl/ICreateTypeInfo::SetAlignment
f1_keywords:
- oaidl/ICreateTypeInfo.SetAlignment
dev_langs:
- c++
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- oaidl.h
api_name:
- ICreateTypeInfo.SetAlignment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateTypeInfo::SetAlignment


## -description


Specifies the data alignment for an item of TYPEKIND=TKIND_RECORD.


## -parameters




### -param cbAlignment [in]

Alignment method for the type. A value of 0 indicates alignment on the 64K boundary; 1 indicates no special alignment. For other values, n indicates alignment on byte <i>n</i>.



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
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot write to the destination.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.


</td>
</tr>
</table>
 




## -remarks



The alignment is the minimum of the natural alignment (for example, byte data on byte boundaries, word data on word boundaries, and so on), and the alignment denoted by <i>cbAlignment</i>.





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>
 

 

