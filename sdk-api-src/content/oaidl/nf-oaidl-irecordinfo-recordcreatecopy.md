---
UID: NF:oaidl.IRecordInfo.RecordCreateCopy
title: IRecordInfo::RecordCreateCopy
author: windows-driver-content
description: Creates a copy of an instance of a record to the specified location.
old-location: automat\irecordinfo_recordcreatecopy.htm
old-project: automat
ms.assetid: 9cc2a46a-ec92-46a7-8b75-8c36598cc441
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IRecordInfo interface [Automation],RecordCreateCopy method, IRecordInfo.RecordCreateCopy, IRecordInfo::RecordCreateCopy, RecordCreateCopy, RecordCreateCopy method [Automation], RecordCreateCopy method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordCreateCopy, automat.irecordinfo_recordcreatecopy, oaidl/IRecordInfo::RecordCreateCopy
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
-	IRecordInfo.RecordCreateCopy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRecordInfo::RecordCreateCopy


## -description


Creates a copy of an instance of a record to the specified location.




## -parameters




### -param pvSource [in]

An instance of the record to be copied.



### -param ppvDest [out]

The new record with data copied from <i>pvSource</i>.


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
</table>
 




## -remarks



The records created must be freed by calling <a href="https://msdn.microsoft.com/36faf2f6-ecb5-4d6f-a05d-a37ae21a8f07">RecordDestroy</a>.




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>
 

 

