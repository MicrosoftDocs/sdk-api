---
UID: NF:oaidl.IRecordInfo.GetGuid
title: IRecordInfo::GetGuid
author: windows-sdk-content
description: Gets the GUID of the record type.
old-location: automat\irecordinfo_getguid.htm
tech.root: automat
ms.assetid: e28ed38a-5cd6-4edb-871e-e69283e4d47e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetGuid, GetGuid method [Automation], GetGuid method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetGuid method, IRecordInfo.GetGuid, IRecordInfo::GetGuid, _oa96_IRecordInfo_GetGuid, automat.irecordinfo_getguid, oaidl/IRecordInfo::GetGuid
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
 - IRecordInfo.GetGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRecordInfo::GetGuid


## -description


Gets the GUID of the record type.




## -parameters




### -param pguid [out]

The class GUID of the TypeInfo that describes the UDT.


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
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.


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
 

 

