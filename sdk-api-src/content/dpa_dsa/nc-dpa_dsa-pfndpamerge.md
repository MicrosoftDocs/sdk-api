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

# PFNDPAMERGE callback function


## -description


Defines the prototype for the merge function used by <a href="https://msdn.microsoft.com/c2d8ffab-1cd1-4328-9740-524c39b6821c">DPA_Merge</a>.


## -parameters




### -param uMsg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A message that instructs this function how to handle the merge. One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DPAMM_MERGE"></a><a id="dpamm_merge"></a><dl>
<dt><b>DPAMM_MERGE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Perform any additional processing needed when merging <i>pvSrc</i> into <i>pvDest</i>. The function should return a pointer to an item that contains the result of the merge. The value returned by the merge function is stored into the destination, which overwrites the previous value. If the merge function returns <b>NULL</b>, then the merge operation is abandoned.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAMM_DELETE"></a><a id="dpamm_delete"></a><dl>
<dt><b>DPAMM_DELETE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Perform any additional processing needed when a delete occurs as part of the merge. The function should return <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAMM_INSERT"></a><a id="dpamm_insert"></a><dl>
<dt><b>DPAMM_INSERT</b></dt>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
Perform any user-defined processing when the merge results in an item being inserted as part of the merge. The return value of this function should point to the item result that is inserted as part of the merge. If the merge function returns <b>NULL</b>, then the merge operation is abandoned.

</td>
</tr>
</table>
 


### -param *pvDest [in]

Type: <b>void*</b>

A pointer to the first item in the merge.


### -param *pvSrc [in]

Type: <b>void*</b>

A pointer to the second item in the merge.


### -param lParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Additional data that can be used by the merge callback.


## -returns



A pointer to the item which results from the merge or <b>NULL</b> if there is a failure when <b>DPAMM_MERGE</b> or <b>DPAMM_INSERT</b> is used.




## -remarks



The callback function might not modify the dynamic pointer arrays (DPAs) involved in the merge operation.




## -see-also




<a href="https://msdn.microsoft.com/2ae5f250-c79e-4ca5-98c4-b15ed7d5b90a">PFNDPAMERGECONST</a>
 

 

