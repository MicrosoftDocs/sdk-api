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

# ITfLangBarItemMgr::GetItems


## -description




## -parameters




### -param ulCount [in]

Specifies the number of items to obtain the status for.


### -param ppItem [out]

Pointer to an array of <a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a> interface pointers that receive the item interfaces. This array must be at least <i>ulCount</i> elements in length.


### -param pInfo

[in, out] Pointer to an array of <a href="https://msdn.microsoft.com/4a826a2c-4cae-4cbf-8a25-38337dcd498d">TF_LANGBARITEMINFO</a> structures that receive the information for each item. This array must be at least <i>ulCount</i> elements in length.


### -param pdwStatus

[in, out] Pointer to an array of <b>DWORD</b> values that receive the status of each item. Each element in this array receives zero or a combination of one or more of the <a href="https://msdn.microsoft.com/5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc">TF_LBI_STATUS_*</a> values. This array must be at least <i>ulCount</i> elements in length.


### -param pcFetched

[in, out] Pointer to a ULONG that receives the number of items obtained by this method. This parameter can be <b>NULL</b> if this information is not required.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of items obtained is less than the number of items requested. If <i>pcFetched</i> is not <b>NULL</b>, <i>pcFetched</i> receives the number of items obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/4a826a2c-4cae-4cbf-8a25-38337dcd498d">TF_LANGBARITEMINFO</a>



<a href="https://msdn.microsoft.com/5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc">TF_LBI_STATUS_* Constants
      </a>
 

 

