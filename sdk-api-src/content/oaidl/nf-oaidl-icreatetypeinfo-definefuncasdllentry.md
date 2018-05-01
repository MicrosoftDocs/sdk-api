---
UID: NF:oaidl.ICreateTypeInfo.DefineFuncAsDllEntry
title: ICreateTypeInfo::DefineFuncAsDllEntry method
author: windows-driver-content
description: Associates a DLL entry point with the function that has the specified index.
old-location: automat\icreatetypeinfo_definefuncasdllentry.htm
old-project: automat
ms.assetid: 47ec09af-0642-4645-b946-acabbb7c028a
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: DefineFuncAsDllEntry method [Automation], DefineFuncAsDllEntry method [Automation], ICreateTypeInfo interface, DefineFuncAsDllEntry,ICreateTypeInfo.DefineFuncAsDllEntry, ICreateTypeInfo, ICreateTypeInfo interface [Automation], DefineFuncAsDllEntry method, ICreateTypeInfo::DefineFuncAsDllEntry, _oa96_ICreateTypeInfo_DefineFuncAsDllEntry, automat.icreatetypeinfo_definefuncasdllentry, oaidl/ICreateTypeInfo::DefineFuncAsDllEntry
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
-	ICreateTypeInfo.DefineFuncAsDllEntry
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ICreateTypeInfo::DefineFuncAsDllEntry method


## -description


Associates a DLL entry point with the function that has the specified index.


## -parameters




### -param index [in]

The index of the function.


### -param szDllName [in]

The name of the DLL that contains the entry point.




### -param szProcName [in]

The name of the entry point or an ordinal (if the high word is zero).



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
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The element cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_WRONGTYPEKIND</b></dt>
</dl>
</td>
<td width="60%">
Type mismatch.

</td>
</tr>
</table>
 




## -remarks



If the high word of <i>szProcName</i> is zero, then the low word must contain the ordinal of the entry point; otherwise, <i>szProcName</i> points to the zero-terminated name of the entry point.





## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

