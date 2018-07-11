---
UID: NF:oaidl.ICreateTypeLib2.SetHelpStringContext
title: ICreateTypeLib2::SetHelpStringContext
author: windows-sdk-content
description: Sets the Help string context number.
old-location: automat\icreatetypelib2_sethelpstringcontext.htm
old-project: automat
ms.assetid: 35093252-74ff-4161-bf3d-f5e6b69e73c1
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: ICreateTypeLib2 interface [Automation],SetHelpStringContext method, ICreateTypeLib2.SetHelpStringContext, ICreateTypeLib2::SetHelpStringContext, SetHelpStringContext, SetHelpStringContext method [Automation], SetHelpStringContext method [Automation],ICreateTypeLib2 interface, _oa96_ICreateTypeLib2_SetHelpStringContext, automat.icreatetypelib2_sethelpstringcontext, oaidl/ICreateTypeLib2::SetHelpStringContext
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
 - ICreateTypeLib2.SetHelpStringContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeLib2::SetHelpStringContext


## -description


Sets the Help string context number.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/97378353-8c2d-493a-8ee9-42d33ab47d18">ICreateTypeLib2</a>
 

 

