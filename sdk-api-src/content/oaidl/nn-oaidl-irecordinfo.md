---
UID: NN:oaidl.IRecordInfo
title: IRecordInfo
author: windows-driver-content
description: Describes the structure of a particular UDT.
old-location: automat\irecordinfo.htm
old-project: automat
ms.assetid: 065ebfa8-bfac-4c75-a3f9-9dc0409ea454
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IRecordInfo, IRecordInfo interface [Automation], IRecordInfo interface [Automation],described, _oa96_IRecordInfo_Interface, automat.irecordinfo, oaidl/IRecordInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IRecordInfo
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRecordInfo interface


## -description


Describes the structure of a particular UDT. You can use <b>IRecordInfo</b> any time you need to access the description of UDTs contained in type libraries. <b>IRecordInfo</b> can be reused as needed; there can be many instances of the UDT for a single <b>IRecordInfo</b> pointer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRecordInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRecordInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRecordInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6765371c-209a-4794-bff8-83560171affb">GetField</a>
</td>
<td align="left" width="63%">
Returns a pointer to the VARIANT containing the value of a given field name.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cf4f149-1cdc-4884-887a-0eb44eeab8ff">GetFieldNames</a>
</td>
<td align="left" width="63%">
Gets the names of the fields of the record.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3775fa60-3f34-402f-a7e5-18a00de384b5">GetFieldNoCopy</a>
</td>
<td align="left" width="63%">
Returns a pointer to the value of a given field name without copying the value and allocating resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e28ed38a-5cd6-4edb-871e-e69283e4d47e">GetGuid</a>
</td>
<td align="left" width="63%">
Gets the GUID of the record type.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b769f792-45cb-4070-9be7-0b95b17a9ed8">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the record type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca0f43b2-2b8f-4b22-8674-8223f0c607ab">GetSize</a>
</td>
<td align="left" width="63%">
Gets the number of bytes of memory necessary to hold the record instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8c05c4a-000a-4e48-aace-ff9f9292e3ea">GetTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the type information that describes a UDT or safearray of UDTs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3db29912-3864-4750-b255-77dcffe711cf">IsMatchingType</a>
</td>
<td align="left" width="63%">
Determines whether the record that is passed in matches that of the current record information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/784bb283-b381-405e-b793-d070105b778f">PutField</a>
</td>
<td align="left" width="63%">
Puts a variant into a field.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e3c4189-46fa-4c21-abbd-35fdd5df058d">PutFieldNoCopy</a>
</td>
<td align="left" width="63%">
 Passes ownership of the data to the assigned field by placing the actual data into the field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/979b0702-3342-4036-8113-c84728436ab6">RecordClear</a>
</td>
<td align="left" width="63%">
Releases object references and other values of a record without deallocating the record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e5a57a2-06d1-47b3-8e3c-c8718b550bcb">RecordCopy</a>
</td>
<td align="left" width="63%">
Copies an existing record into the passed in buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f688623e-c03b-456f-bd51-426049e0eb2b">RecordCreate</a>
</td>
<td align="left" width="63%">
Allocates memory for a new record, initializes the instance and returns a pointer to the record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cc2a46a-ec92-46a7-8b75-8c36598cc441">RecordCreateCopy</a>
</td>
<td align="left" width="63%">
Creates a copy of an instance of a record to the specified location.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36faf2f6-ecb5-4d6f-a05d-a37ae21a8f07">RecordDestroy</a>
</td>
<td align="left" width="63%">
Releases the resources and deallocates the memory of the record. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e10355b3-b751-487d-b7ce-77a39803c38c">RecordInit</a>
</td>
<td align="left" width="63%">
Initializes a new instance of a record. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/badf90a3-82b6-4f2d-8f85-da159e5a1988">UDT Functions and Interfaces</a>



<a href="https://msdn.microsoft.com/66fde40c-1e22-4697-a658-fa1e749cebb3">User-Defined Data Types </a>
 

 

