---
UID: NF:oaidl.IRecordInfo.GetFieldNames
title: IRecordInfo::GetFieldNames
author: windows-sdk-content
description: Gets the names of the fields of the record.
old-location: automat\irecordinfo_getfieldnames.htm
tech.root: automat
ms.assetid: 1cf4f149-1cdc-4884-887a-0eb44eeab8ff
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetFieldNames, GetFieldNames method [Automation], GetFieldNames method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetFieldNames method, IRecordInfo.GetFieldNames, IRecordInfo::GetFieldNames, _oa96_IRecordInfo_GetFieldNames, automat.irecordinfo_getfieldnames, oaidl/IRecordInfo::GetFieldNames
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
 - IRecordInfo.GetFieldNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRecordInfo::GetFieldNames


## -description


Gets the names of the fields of the record.




## -parameters




### -param pcNames [in, out]

The number of names to return.


### -param rgBstrNames [out]

The name of the array of type BSTR.

If the <i>rgBstrNames</i> parameter is NULL, then <i>pcNames</i> is returned with the number of field names. 

It the <i>rgBstrNames</i> parameter is not NULL, then the string names contained in <i>rgBstrNames</i> are returned. If the number of names in <i>pcNames</i> and <i>rgBstrNames</i> are not equal then the lesser number of the two is the number of returned field names. The caller needs to free the BSTRs inside the array returned in <i>rgBstrNames</i>.


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



The caller should allocate memory for the array of BSTRs. If the array is larger than needed, set the unused portion to 0.

On return, the caller will need to free each contained BSTR using <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.

In case of out of memory, <i>pcNames</i> points to error code.




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>



<a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

