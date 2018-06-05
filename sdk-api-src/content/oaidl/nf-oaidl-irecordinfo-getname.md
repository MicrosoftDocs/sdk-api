---
UID: NF:oaidl.IRecordInfo.GetName
title: IRecordInfo::GetName
author: windows-sdk-content
description: Gets the name of the record type.
old-location: automat\irecordinfo_getname.htm
old-project: automat
ms.assetid: b769f792-45cb-4070-9be7-0b95b17a9ed8
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetName, GetName method [Automation], GetName method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetName method, IRecordInfo.GetName, IRecordInfo::GetName, _oa96_IRecordInfo_GetName, automat.irecordinfo_getname, oaidl/IRecordInfo::GetName
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	IRecordInfo.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRecordInfo::GetName


## -description


Gets the name of the record type. This is useful if you want to print out the type of the record, because each UDT has it's own <a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>.


## -parameters




### -param pbstrName [out]

The name.


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
<dt><b>E_OUT_OFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

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
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.


</td>
</tr>
</table>
 




## -remarks



The caller must free the BSTR by calling <a href="8F230EE3-5F6E-4CB9-A910-9C90B754DCD3">SysFreeString</a>.




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>
 

 

