---
UID: NF:oaidl.ICreateTypeInfo2.SetImplTypeCustData
title: ICreateTypeInfo2::SetImplTypeCustData
author: windows-sdk-content
description: Sets a value for custom data for the specified implementation type.
old-location: automat\icreatetypeinfo2_setimpltypecustdata.htm
tech.root: automat
ms.assetid: f9dee7fc-b713-4a68-a8ea-2398a266e728
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetImplTypeCustData method, ICreateTypeInfo2.SetImplTypeCustData, ICreateTypeInfo2::SetImplTypeCustData, SetImplTypeCustData, SetImplTypeCustData method [Automation], SetImplTypeCustData method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetImplTypeCustData, automat.icreatetypeinfo2_setimpltypecustdata, oaidl/ICreateTypeInfo2::SetImplTypeCustData
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICreateTypeInfo2.SetImplTypeCustData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateTypeInfo2::SetImplTypeCustData


## -description


Sets a value for custom data for the specified implementation type.


## -parameters




### -param index [in]

The index of the variable for which to set the custom data.


### -param guid [in]

The unique identifier used to identify the data.


### -param pVarVal [in]

The data to store (any variant except an object).



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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/34dc6f52-6864-4edb-b22d-80eef05d4c8c">ICreateTypeInfo2</a>
 

 

