---
UID: NF:oaidl.IRecordInfo.PutFieldNoCopy
title: IRecordInfo::PutFieldNoCopy
author: windows-sdk-content
description: Passes ownership of the data to the assigned field by placing the actual data into the field.
old-location: automat\irecordinfo_putfieldnocopy.htm
old-project: automat
ms.assetid: 9e3c4189-46fa-4c21-abbd-35fdd5df058d
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IRecordInfo interface [Automation],PutFieldNoCopy method, IRecordInfo.PutFieldNoCopy, IRecordInfo::PutFieldNoCopy, PutFieldNoCopy, PutFieldNoCopy method [Automation], PutFieldNoCopy method [Automation],IRecordInfo interface, _oa96_IRecordInfo_PutFieldNoCopy, automat.irecordinfo_putfieldnocopy, oaidl/IRecordInfo::PutFieldNoCopy
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
-	IRecordInfo.PutFieldNoCopy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRecordInfo::PutFieldNoCopy


## -description


 Passes ownership of the data to the assigned field by placing the actual data into the field.<b>PutFieldNoCopy</b> is useful for saving resources because it allows you to place your data directly into a record field. <b>PutFieldNoCopy</b> differs from <a href="https://msdn.microsoft.com/784bb283-b381-405e-b793-d070105b778f">PutField</a> because it does not copy the data referenced by the variant.


## -parameters




### -param wFlags [in]

The only legal values for the wFlags parameter is INVOKE_PROPERTYPUT or INVOKE_PROPERTYPUTREF.


### -param pvData [in, out]

An instance of the record described by <a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>.



### -param szFieldName [in]

The name of the field of the record.



### -param pvarField [in]

The variant to be put into the field.


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
 




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>
 

 

