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

# DrtContinueSearch function


## -description


The <b>DrtContinueSearch</b> function continues an iterative search for a key.This function is used only when the <b>fIterative</b> flag is set to 'true' in the associated <a href="https://msdn.microsoft.com/a3f12d8a-95ef-4168-8d2d-c317ae2c57b4">DRT_SEARCH_INFO</a> structure. Call this after getting a <b>DRT_MATCH_INTERMEDIATE</b> search result.


## -parameters




### -param hSearchContext [in]

Handle to the search context  to close. This parameter is returned by the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> API.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hSearchContext</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This search is not an iterative search.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a3f12d8a-95ef-4168-8d2d-c317ae2c57b4">DRT_SEARCH_INFO</a>



<a href="https://msdn.microsoft.com/1a99476f-69ee-4aeb-8c9b-e06315ec095d">DrtEndSearch</a>



<a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a>
 

 

