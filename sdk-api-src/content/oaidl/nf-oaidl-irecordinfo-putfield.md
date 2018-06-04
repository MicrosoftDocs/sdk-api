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

# IRecordInfo::PutField


## -description


Puts a variant into a field.




## -parameters




### -param wFlags [in]

The only legal values for the wFlags parameter is INVOKE_PROPERTYPUT or INVOKE_PROPERTYPUTREF.

If INVOKE_PROPERTYPUTREF is passed in then <b>PutField</b> just assigns the value of the variant that is passed in to the field using normal coercion rules.

If INVOKE_PROPERTYPUT is passed in then specific rules apply. If the field is declared as a class that derives from <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and the field's value is NULL then an error will be returned. If the field's value is not NULL then the variant will be passed to the default property supported by the object referenced by the field. If the field is not declared as a class derived from <b>IDispatch</b> then an error will be returned. If the field is declared as a variant of type VT_Dispatch then the default value of the object is assigned to the field. Otherwise, the variant's value is assigned to the field. 


### -param pvData [in, out]

The pointer to an instance of the record.


### -param szFieldName [in]

The name of the field of the record.


### -param pvarField [in]

The pointer to the variant.


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
 

 

