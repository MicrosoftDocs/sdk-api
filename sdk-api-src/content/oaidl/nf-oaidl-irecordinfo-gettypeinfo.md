---
UID: NF:oaidl.IRecordInfo.GetTypeInfo
title: IRecordInfo::GetTypeInfo
author: windows-sdk-content
description: Retrieves the type information that describes a UDT or safearray of UDTs.
old-location: automat\irecordinfo_gettypeinfo.htm
old-project: automat
ms.assetid: c8c05c4a-000a-4e48-aace-ff9f9292e3ea
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetTypeInfo, GetTypeInfo method [Automation], GetTypeInfo method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetTypeInfo method, IRecordInfo.GetTypeInfo, IRecordInfo::GetTypeInfo, _oa96_IRecordInfo_GetTypeInfo, automat.irecordinfo_gettypeinfo, oaidl/IRecordInfo::GetTypeInfo
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
-	IRecordInfo.GetTypeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRecordInfo::GetTypeInfo


## -description


Retrieves the type information that describes a UDT or safearray of UDTs.


## -parameters




### -param ppTypeInfo [out]

The information type of the record.


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



<b>AddRef</b> is called on the pointer <i>ppTypeInfo</i>.




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>



<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

