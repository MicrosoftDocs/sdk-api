---
UID: NF:oleauto.GetRecordInfoFromTypeInfo
title: GetRecordInfoFromTypeInfo function
author: windows-driver-content
description: Returns a pointer to the IRecordInfo interface of the UDT by passing its type information.
old-location: automat\getrecordinfofromtypeinfo.htm
old-project: automat
ms.assetid: 9bf2803f-7a6c-4574-80d2-4069f5b81057
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetRecordInfoFromTypeInfo, GetRecordInfoFromTypeInfo function [Automation], _oa96_GetRecordInfoFromTypeInfo, automat.getrecordinfofromtypeinfo, oleauto/GetRecordInfoFromTypeInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	GetRecordInfoFromTypeInfo
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# GetRecordInfoFromTypeInfo function


## -description


Returns a pointer to the <a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a> interface of the UDT by passing its type information. The given <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> interface is used to create a RecordInfo object.


## -parameters




### -param pTypeInfo [in]

The type information of a record.



### -param ppRecInfo [out]

The <a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a> interface.


## -returns



This function can return one of these values.

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
<dt><b>E_OUTOFMEMORY
</b></dt>
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
<dt><b>TYPE_E_UNSUPFORMAT
</b></dt>
</dl>
</td>
<td width="60%">
The type is not an interface.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>



<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

