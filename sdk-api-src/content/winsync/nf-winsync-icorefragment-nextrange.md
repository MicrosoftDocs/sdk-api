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

# ICoreFragment::NextRange


## -description


Returns the next range that is contained in this knowledge fragment, and the clock vector that defines what is known about the items in the range.


## -parameters




### -param pItemId [in, out]

Returns the closed lower bound of item IDs in this range. This value is also the open upper bound of item IDs in the previous range when it is not the first in the range set.


### -param pItemIdSize [in, out]

Specifies the number of bytes in <i>pItemId</i>. Returns the number of bytes written, or the number of bytes that are required to retrieve the ID when <i>pItemId</i> is too small.


### -param piClockVector [out]

Returns the clock vector that defines what is known about the items in the range.


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
There are no more ranges to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The item ID is a variable-length ID and <i>pItemIdSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pItemId</i> is too small. In this situation, the required number of bytes is returned in <i>pItemIdSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object that is contained in this object has changed since this object was created.

</td>
</tr>
</table>
 




## -remarks



The value that is returned in <i>pItemId</i> is the closed lower bound on the range of item IDs that are associated with the clock vector that is returned in <i>piClockVector</i>. The value of <i>pItemId</i> also defines the open upper bound of the previous range, so the open upper bound of the current range can be obtained by calling <b>NextRange</b> again. If there are no more ranges to enumerate, the range contains all items that have IDs greater than or equal to <i>pItemId</i>.




## -see-also




<a href="https://msdn.microsoft.com/3e232531-ad44-4ad1-b186-46edbc07291b">ICoreFragment Interface</a>
 

 

