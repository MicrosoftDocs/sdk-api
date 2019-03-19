---
UID: NF:oaidl.ICreateTypeInfo2.SetHelpStringContext
title: ICreateTypeInfo2::SetHelpStringContext (oaidl.h)
author: windows-sdk-content
description: Sets the context number for the specified Help string.
old-location: automat\icreatetypeinfo2_sethelpstringcontext.htm
tech.root: automat
ms.assetid: 2f8ed63a-1cbb-4fd3-a848-aeb8123adf04
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetHelpStringContext method, ICreateTypeInfo2.SetHelpStringContext, ICreateTypeInfo2::SetHelpStringContext, SetHelpStringContext, SetHelpStringContext method [Automation], SetHelpStringContext method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetHelpStringContext, automat.icreatetypeinfo2_sethelpstringcontext, oaidl/ICreateTypeInfo2::SetHelpStringContext
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
 - ICreateTypeInfo2.SetHelpStringContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateTypeInfo2::SetHelpStringContext


## -description


Sets the context number for the specified Help string.


## -parameters




### -param dwHelpStringContext [in]

 The Help string context number.


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
 

 

