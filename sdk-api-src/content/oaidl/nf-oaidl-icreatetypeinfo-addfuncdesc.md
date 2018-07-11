---
UID: NF:oaidl.ICreateTypeInfo.AddFuncDesc
title: ICreateTypeInfo::AddFuncDesc
author: windows-sdk-content
description: Adds a function description to the type description.
old-location: automat\icreatetypeinfo_addfuncdesc.htm
old-project: automat
ms.assetid: f6816778-86f6-4e59-8eb2-444fd7bd6354
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: AddFuncDesc, AddFuncDesc method [Automation], AddFuncDesc method [Automation],ICreateTypeInfo interface, ICreateTypeInfo interface [Automation],AddFuncDesc method, ICreateTypeInfo.AddFuncDesc, ICreateTypeInfo::AddFuncDesc, _oa96_ICreateTypeInfo_AddFuncDesc, automat.icreatetypeinfo_addfuncdesc, oaidl/ICreateTypeInfo::AddFuncDesc
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
 - ICreateTypeInfo.AddFuncDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeInfo::AddFuncDesc


## -description


Adds a function description to the type description.


## -parameters




### -param index [in]

The index of the new FUNCDESC in the type information.




### -param pFuncDesc [in]

A FUNCDESC structure that describes the function. The <b>bstrIDLInfo</b> field in the FUNCDESC should be null.


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



The index specifies the order of the functions within the type information. The first function has an index of zero. If an index is specified that exceeds one less than the number of functions in the type information, an error is returned. Calling this function does not pass ownership of the FUNCDESC structure to <a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>. Therefore, the caller must still de-allocate the FUNCDESC structure.



The passed-in virtual function table (VTBL) field (oVft) of the FUNCDESC is ignored if the TYPEKIND is TKIND_MODULE or if oVft is -1 or 0. This attribute is set when <a href="https://msdn.microsoft.com/3880aad3-8a6f-43e6-8420-25c4d1b9a71a">ICreateTypeInfo::LayOut</a> is called. The oVft value is used if the TYPEKIND is TKIND_DISPATCH and a dual interface or if the TYPEKIND is TKIND_INTERFACE. If the oVft is used, it must be a multiple of the sizeof(VOID *) on the machine, otherwise the function fails and E_INVALIDARG is returned as the HRESULT.



The function <b>AddFuncDesc</b> uses the passed-in member identifier (<i>memid</i>) fields within each FUNCDESC for classes with TYPEKIND = TKIND_DISPATCH or TKIND_INTERFACE. If the member IDs are set to MEMBERID_NIL, <b>AddFuncDesc</b> assigns member IDs to the functions. Otherwise, the member ID fields within each FUNCDESC are ignored.



Any HREFTYPE fields in the FUNCDESC structure must have been produced by the same instance of <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> for which <b>AddFuncDesc</b> is called.



The get and put accessor functions for the same property must have the same dispatch identifier (DISPID).





## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

