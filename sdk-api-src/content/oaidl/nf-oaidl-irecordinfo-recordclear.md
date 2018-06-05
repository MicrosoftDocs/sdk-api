---
UID: NF:oaidl.IRecordInfo.RecordClear
title: IRecordInfo::RecordClear
author: windows-sdk-content
description: Releases object references and other values of a record without deallocating the record.
old-location: automat\irecordinfo_recordclear.htm
old-project: automat
ms.assetid: 979b0702-3342-4036-8113-c84728436ab6
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IRecordInfo interface [Automation],RecordClear method, IRecordInfo.RecordClear, IRecordInfo::RecordClear, RecordClear, RecordClear method [Automation], RecordClear method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordClear, automat.irecordinfo_recordclear, oaidl/IRecordInfo::RecordClear
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
-	IRecordInfo.RecordClear
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRecordInfo::RecordClear


## -description


Releases object references and other values of a record without deallocating the record.


## -parameters




### -param pvExisting [in]

The record to be cleared.


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



<b>RecordClear</b> releases memory blocks held by VT_PTR or VT_SAFEARRAY instance fields. The caller needs to free the instance fields memory, <b>RecordClear</b> will do nothing if there are no resources held. 




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>
 

 

