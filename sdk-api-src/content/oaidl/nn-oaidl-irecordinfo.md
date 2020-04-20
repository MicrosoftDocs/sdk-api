---
UID: NN:oaidl.IRecordInfo
title: IRecordInfo (oaidl.h)
description: Describes the structure of a particular UDT.helpviewer_keywords: ["IRecordInfo","IRecordInfo interface [Automation]","IRecordInfo interface [Automation]","described","_oa96_IRecordInfo_Interface","automat.irecordinfo","oaidl/IRecordInfo"]
old-location: automat\irecordinfo.htm
tech.root: automat
ms.assetid: 065ebfa8-bfac-4c75-a3f9-9dc0409ea454
ms.date: 12/05/2018
ms.keywords: IRecordInfo, IRecordInfo interface [Automation], IRecordInfo interface [Automation],described, _oa96_IRecordInfo_Interface, automat.irecordinfo, oaidl/IRecordInfo
f1_keywords:
- oaidl/IRecordInfo
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- oaidl.h
api_name:
- IRecordInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRecordInfo interface


## -description


Describes the structure of a particular UDT. You can use <b>IRecordInfo</b> any time you need to access the description of UDTs contained in type libraries. <b>IRecordInfo</b> can be reused as needed; there can be many instances of the UDT for a single <b>IRecordInfo</b> pointer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRecordInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRecordInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getfield">GetField</a>
</td>
<td align="left" width="63%">
Returns a pointer to the VARIANT containing the value of a given field name.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getfieldnames">GetFieldNames</a>
</td>
<td align="left" width="63%">
Gets the names of the fields of the record.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getfieldnocopy">GetFieldNoCopy</a>
</td>
<td align="left" width="63%">
Returns a pointer to the value of a given field name without copying the value and allocating resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getguid">GetGuid</a>
</td>
<td align="left" width="63%">
Gets the GUID of the record type.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the record type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Gets the number of bytes of memory necessary to hold the record instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-gettypeinfo">GetTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the type information that describes a UDT or safearray of UDTs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-ismatchingtype">IsMatchingType</a>
</td>
<td align="left" width="63%">
Determines whether the record that is passed in matches that of the current record information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-putfield">PutField</a>
</td>
<td align="left" width="63%">
Puts a variant into a field.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-putfieldnocopy">PutFieldNoCopy</a>
</td>
<td align="left" width="63%">
 Passes ownership of the data to the assigned field by placing the actual data into the field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordclear">RecordClear</a>
</td>
<td align="left" width="63%">
Releases object references and other values of a record without deallocating the record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordcopy">RecordCopy</a>
</td>
<td align="left" width="63%">
Copies an existing record into the passed in buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordcreate">RecordCreate</a>
</td>
<td align="left" width="63%">
Allocates memory for a new record, initializes the instance and returns a pointer to the record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordcreatecopy">RecordCreateCopy</a>
</td>
<td align="left" width="63%">
Creates a copy of an instance of a record to the specified location.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recorddestroy">RecordDestroy</a>
</td>
<td align="left" width="63%">
Releases the resources and deallocates the memory of the record. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordinit">RecordInit</a>
</td>
<td align="left" width="63%">
Initializes a new instance of a record. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/udt-functions-and-interfaces">UDT Functions and Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/user-defined-data-types">User-Defined Data Types </a>
 

 

