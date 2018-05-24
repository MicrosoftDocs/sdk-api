---
UID: NF:oaidl.IRecordInfo.RecordCopy
title: IRecordInfo::RecordCopy
author: windows-driver-content
description: Copies an existing record into the passed in buffer.
old-location: automat\irecordinfo_recordcopy.htm
old-project: automat
ms.assetid: 0e5a57a2-06d1-47b3-8e3c-c8718b550bcb
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IRecordInfo interface [Automation],RecordCopy method, IRecordInfo.RecordCopy, IRecordInfo::RecordCopy, RecordCopy, RecordCopy method [Automation], RecordCopy method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordCopy, automat.irecordinfo_recordcopy, oaidl/IRecordInfo::RecordCopy
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
-	IRecordInfo.RecordCopy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRecordInfo::RecordCopy


## -description


Copies an existing record into the passed in buffer.


## -parameters




### -param pvExisting [in]

The current record instance.


### -param pvNew [out]

The destination where the record will be copied.


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
</table>
 




## -remarks



<b>RecordCopy</b> will release the resources in the destination first. The caller is responsible for allocating sufficient memory in the destination by calling <a href="https://msdn.microsoft.com/ca0f43b2-2b8f-4b22-8674-8223f0c607ab">GetSize</a> or  <a href="https://msdn.microsoft.com/f688623e-c03b-456f-bd51-426049e0eb2b">RecordCreate</a>. If <b>RecordCopy</b> fails to copy any of the fields then all fields will be cleared, as though <a href="https://msdn.microsoft.com/979b0702-3342-4036-8113-c84728436ab6">RecordClear</a> had been called.




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>
 

 

