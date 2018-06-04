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

# ICoreFragment::NextColumn


## -description


Returns the next change unit ID in the set of change unit IDs that this knowledge fragment applies to.


## -parameters




### -param pChangeUnitId [in, out]

Returns the next change unit ID in the set.


### -param pChangeUnitIdSize [in, out]

Specifies the number of bytes in <i>pChangeUnitId</i>. Returns the number of bytes written, or the number of bytes that are required to retrieve the ID when <i>pChangeUnitId</i> is too small.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more change unit IDs to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The change unit ID is a variable-length ID and <i>pChangeUnitIdSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pChangeUnitId</i> is too small. In this situation, the required number of bytes is returned in <i>pChangeUnitIdSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object contained within this object has changed since this object was created.

</td>
</tr>
</table>
 




## -remarks



An <b>ISyncKnowledge2</b> object contains one or more <b>ICoreFragment</b> objects, each of which contains knowledge that applies to a specific set of columns. Typically, one of the <b>ICoreFragment</b> objects contains no columns, and its knowledge applies to all of the change units that are not specified in any other fragment. In this situation, <b>NextColumn</b> always returns <b>S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e232531-ad44-4ad1-b186-46edbc07291b">ICoreFragment Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge2 Interface</a>
 

 

