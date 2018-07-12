---
UID: NF:oaidl.ICreateTypeInfo.SetDocString
title: ICreateTypeInfo::SetDocString
author: windows-sdk-content
description: Sets the documentation string displayed by type browsers.
old-location: automat\icreatetypeinfo_setdocstring.htm
old-project: automat
ms.assetid: 927c449b-1d38-4449-a1fd-63fb82c0d660
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetDocString method, ICreateTypeInfo.SetDocString, ICreateTypeInfo::SetDocString, SetDocString, SetDocString method [Automation], SetDocString method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetDocString, automat.icreatetypeinfo_setdocstring, oaidl/ICreateTypeInfo::SetDocString
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
 - ICreateTypeInfo.SetDocString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeInfo::SetDocString


## -description


 Sets the documentation string displayed by type browsers.


## -parameters




### -param pStrDoc [in]

A brief description of the type description.


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
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot write to the destination.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY
</b></dt>
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
 




## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

