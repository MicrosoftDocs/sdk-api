---
UID: NF:oaidl.ICreateTypeLib.SetLibFlags
title: ICreateTypeLib::SetLibFlags
author: windows-sdk-content
description: Sets library flags.
old-location: automat\icreatetypelib_setlibflags.htm
old-project: automat
ms.assetid: fc72635c-853f-4a0a-9869-263e4aa39b8b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICreateTypeLib interface [Automation],SetLibFlags method, ICreateTypeLib.SetLibFlags, ICreateTypeLib::SetLibFlags, SetLibFlags, SetLibFlags method [Automation], SetLibFlags method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetLibFlags, automat.icreatetypelib_setlibflags, oaidl/ICreateTypeLib::SetLibFlags
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
 - ICreateTypeLib.SetLibFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeLib::SetLibFlags


## -description


Sets library flags.


## -parameters




### -param uLibFlags [in]

The flags to set.


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
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.

</td>
</tr>
</table>
 




## -remarks



Valid <i>uLibFlags</i> values are listed in <a href="2C5ECBAF-CE6C-4BE1-A3FA-1066DD6E716D">LIBFLAGS</a>. 




## -see-also




<a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a>
 

 

