---
UID: NF:oaidl.ICreateTypeInfo2.SetVarHelpStringContext
title: ICreateTypeInfo2::SetVarHelpStringContext
author: windows-sdk-content
description: Sets a Help context value for a specified variable.
old-location: automat\icreatetypeinfo2_setvarhelpstringcontext.htm
tech.root: automat
ms.assetid: 0939e286-150c-4258-bb6a-c020b6323b35
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetVarHelpStringContext method, ICreateTypeInfo2.SetVarHelpStringContext, ICreateTypeInfo2::SetVarHelpStringContext, SetVarHelpStringContext, SetVarHelpStringContext method [Automation], SetVarHelpStringContext method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetVarHelpStringContext, automat.icreatetypeinfo2_setvarhelpstringcontext, oaidl/ICreateTypeInfo2::SetVarHelpStringContext
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
 - ICreateTypeInfo2.SetVarHelpStringContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateTypeInfo2::SetVarHelpStringContext


## -description


Sets a Help context value for a specified variable.


## -parameters




### -param index [in]

The index of the variable.




### -param dwHelpStringContext [in]

The Help string context for a localized string.



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
 

 

