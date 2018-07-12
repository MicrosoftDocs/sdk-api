---
UID: NF:oaidl.ICreateTypeInfo.SetTypeDescAlias
title: ICreateTypeInfo::SetTypeDescAlias
author: windows-sdk-content
description: Sets the type description for which this type description is an alias, if TYPEKIND=TKIND_ALIAS.
old-location: automat\icreatetypeinfo_settypedescalias.htm
old-project: automat
ms.assetid: 63435592-9fc8-4d49-a388-87f1d15f2603
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetTypeDescAlias method, ICreateTypeInfo.SetTypeDescAlias, ICreateTypeInfo::SetTypeDescAlias, SetTypeDescAlias, SetTypeDescAlias method [Automation], SetTypeDescAlias method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetTypeDescAlias, automat.icreatetypeinfo_settypedescalias, oaidl/ICreateTypeInfo::SetTypeDescAlias
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeInfo.SetTypeDescAlias
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeInfo::SetTypeDescAlias


## -description


Sets the type description for which this type description is an alias, if TYPEKIND=TKIND_ALIAS.


## -parameters




### -param pTDescAlias [in]

The type description.


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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

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
<dt><b>TYPE_E_WRONGTYPEKIND</b></dt>
</dl>
</td>
<td width="60%">
Type mismatch.


</td>
</tr>
</table>
 




## -remarks



To set the type for an alias, call <b>SetTypeDescAlias</b> for a type description whose TYPEKIND is TKIND_ALIAS.




## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

