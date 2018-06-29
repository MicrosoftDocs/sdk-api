---
UID: NF:oaidl.ITypeInfo2.GetAllFuncCustData
title: ITypeInfo2::GetAllFuncCustData
author: windows-sdk-content
description: Gets all custom data from the specified function.
old-location: automat\itypeinfo2_getallfunccustdata.htm
old-project: automat
ms.assetid: 65ea243f-fe13-4443-80e9-4b19cf0cb8c8
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetAllFuncCustData, GetAllFuncCustData method [Automation], GetAllFuncCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetAllFuncCustData method, ITypeInfo2.GetAllFuncCustData, ITypeInfo2::GetAllFuncCustData, _oa96_ITypeInfo2_GetAllFuncCustData, automat.itypeinfo2_getallfunccustdata, oaidl/ITypeInfo2::GetAllFuncCustData
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
 - ITypeInfo2.GetAllFuncCustData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeInfo2::GetAllFuncCustData


## -description


Gets all custom data from the specified function.


## -parameters




### -param index [in]

The index of the function for which to get the custom data.




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
 




## -remarks



After the call, the caller needs to release memory used to hold the custom data item by calling <a href="https://msdn.microsoft.com/14556107-3b22-48c8-b480-280b9dee9b17">ClearCustData</a>.




## -see-also




<a href="https://msdn.microsoft.com/d3a34a13-6114-4f15-9de5-60da43fde600">ITypeInfo2</a>
 

 

