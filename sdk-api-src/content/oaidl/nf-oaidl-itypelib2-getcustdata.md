---
UID: NF:oaidl.ITypeLib2.GetCustData
title: ITypeLib2::GetCustData
author: windows-sdk-content
description: Gets the custom data.
old-location: automat\itypelib2_getcustdata.htm
old-project: automat
ms.assetid: e2f29070-6768-4734-a3e2-c9258375b33c
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetCustData, GetCustData method [Automation], GetCustData method [Automation],ITypeLib2 interface, ITypeLib2 interface [Automation],GetCustData method, ITypeLib2.GetCustData, ITypeLib2::GetCustData, _oa96_ITypeLib2_GetCustData, automat.itypelib2_getcustdata, oaidl/ITypeLib2::GetCustData
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
 - ITypeLib2.GetCustData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeLib2::GetCustData


## -description


Gets the custom data.


## -parameters




### -param guid [in]

The GUID used to identify the data.


### -param pVarVal [out]

The retrieved data.


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




<a href="https://msdn.microsoft.com/47561b53-3f7b-4939-8b86-5acb5eaeea5a">ITypeLib2</a>
 

 

