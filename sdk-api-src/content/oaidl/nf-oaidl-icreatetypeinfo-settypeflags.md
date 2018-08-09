---
UID: NF:oaidl.ICreateTypeInfo.SetTypeFlags
title: ICreateTypeInfo::SetTypeFlags
author: windows-sdk-content
description: Sets type flags of the type description being created.
old-location: automat\icreatetypeinfo_settypeflags.htm
old-project: automat
ms.assetid: 7dfc1673-6242-4beb-978f-85f2000fab8e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetTypeFlags method, ICreateTypeInfo.SetTypeFlags, ICreateTypeInfo::SetTypeFlags, SetTypeFlags, SetTypeFlags method [Automation], SetTypeFlags method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetTypeFlags, automat.icreatetypeinfo_settypeflags, oaidl/ICreateTypeInfo::SetTypeFlags
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
 - ICreateTypeInfo.SetTypeFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeInfo::SetTypeFlags


## -description


Sets type flags of the type description being created.


## -parameters




### -param uTypeFlags [in]

The settings for the type flags. For details, see TYPEFLAGS. 


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
 




## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

