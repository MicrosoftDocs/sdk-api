---
UID: NF:oaidl.ITypeInfo2.GetAllImplTypeCustData
title: ITypeInfo2::GetAllImplTypeCustData
author: windows-sdk-content
description: Gets all custom data for the specified implementation type.
old-location: automat\itypeinfo2_getallimpltypecustdata.htm
tech.root: automat
ms.assetid: 021849d8-ec61-4f35-8302-caa8338a8758
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetAllImplTypeCustData, GetAllImplTypeCustData method [Automation], GetAllImplTypeCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetAllImplTypeCustData method, ITypeInfo2.GetAllImplTypeCustData, ITypeInfo2::GetAllImplTypeCustData, _oa96_ITypeInfo2_GetAllImplTypeCustData, automat.itypeinfo2_getallimpltypecustdata, oaidl/ITypeInfo2::GetAllImplTypeCustData
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
 - ITypeInfo2.GetAllImplTypeCustData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeInfo2::GetAllImplTypeCustData


## -description


Gets all custom data for the specified implementation type.


## -parameters




### -param index [in]

The index of the implementation type for the custom data.




### -param pCustData [out]

The custom data items.


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




<a href="https://msdn.microsoft.com/d3a34a13-6114-4f15-9de5-60da43fde600">ITypeInfo2</a>
 

 

