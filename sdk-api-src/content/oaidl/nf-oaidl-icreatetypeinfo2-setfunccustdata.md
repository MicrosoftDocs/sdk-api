---
UID: NF:oaidl.ICreateTypeInfo2.SetFuncCustData
title: ICreateTypeInfo2::SetFuncCustData
author: windows-driver-content
description: Sets a value for custom data for the specified function.
old-location: automat\icreatetypeinfo2_setfunccustdata.htm
old-project: automat
ms.assetid: 553e872f-0620-4b36-a01d-86088bd12f80
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetFuncCustData method, ICreateTypeInfo2.SetFuncCustData, ICreateTypeInfo2::SetFuncCustData, SetFuncCustData, SetFuncCustData method [Automation], SetFuncCustData method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetFuncCustData, automat.icreatetypeinfo2_setfunccustdata, oaidl/ICreateTypeInfo2::SetFuncCustData
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
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	ICreateTypeInfo2.SetFuncCustData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ICreateTypeInfo2::SetFuncCustData


## -description


Sets a value for custom data for the specified function.


## -parameters




### -param index [in]

The index of the function for which to set the custom data.


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
 

 

