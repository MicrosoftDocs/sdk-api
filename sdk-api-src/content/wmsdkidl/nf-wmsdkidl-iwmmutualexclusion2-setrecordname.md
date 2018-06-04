---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMMutualExclusion2::SetRecordName


## -description



The <b>SetRecordName</b> method assigns a name to a record. You should assign a name to every record so that you can easily identify the records in the future.




## -parameters




### -param wRecordNumber [in]

<b>WORD</b> containing the record number to which you want to assign a name.


### -param pwszRecordName [in]

Pointer to a wide-character null-terminated string containing the name you want to assign to the record. Record names are limited to 256 wide characters.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory for the name.

</td>
</tr>
</table>
 




## -remarks



If you pass an empty string as <i>pwszRecordName</i>, the method returns S_OK, but nothing is done.




## -see-also




<a href="https://msdn.microsoft.com/4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf">IWMMutualExclusion2 Interface</a>



<a href="https://msdn.microsoft.com/7508a473-77ae-49ce-b041-2d171193e730">IWMMutualExclusion2::GetRecordName</a>
 

 

