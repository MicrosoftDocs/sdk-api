---
UID: NF:oaidl.ITypeInfo2.GetCustData
title: ITypeInfo2::GetCustData
author: windows-driver-content
description: Gets the custom data.
old-location: automat\itypeinfo2_getcustdata.htm
old-project: automat
ms.assetid: 0c80a357-0967-413f-a211-c3bae8700b36
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetCustData, GetCustData method [Automation], GetCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetCustData method, ITypeInfo2.GetCustData, ITypeInfo2::GetCustData, _oa96_ITypeInfo2_GetCustData, automat.itypeinfo2_getcustdata, oaidl/ITypeInfo2::GetCustData
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
-	ITypeInfo2.GetCustData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITypeInfo2::GetCustData


## -description


Gets the custom data.


## -parameters




### -param guid [in]

The GUID used to identify the data.


### -param pVarVal [out]

The custom data.


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
 

 

