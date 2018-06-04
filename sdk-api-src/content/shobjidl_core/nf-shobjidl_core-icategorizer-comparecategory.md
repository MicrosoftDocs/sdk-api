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

# ICategorizer::CompareCategory


## -description


Determines the relative order of two items in their item identifier lists, and hence in the UI.


## -parameters




### -param csfFlags

Type: <b><a href="https://msdn.microsoft.com/5e3f6c84-ebc4-45e7-8272-f5d98bffd4c8">CATSORT_FLAGS</a></b>

A flag that specifies how the comparison should be performed. The parameter should be one of the values in <a href="https://msdn.microsoft.com/5e3f6c84-ebc4-45e7-8272-f5d98bffd4c8">CATSORT_FLAGS</a>.


### -param dwCategoryId1

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies the first category identifier to use in the comparison.


### -param dwCategoryId2

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies the second category identifier to use in the comparison.


## -returns



Type: <b>HRESULT</b>

If this method is successful, the CODE field of the HRESULT contains a value that specifies the outcome of the comparison, otherwise it returns a COM error code.




## -remarks



The following table shows the values returned in the CODE field of the HRESULT.

    			


<table class="clsStd">
<tr>
<td>Less than zero </td>
<td>The first item should precede the second (<i>dwCategoryId1</i> &lt; <i>dwCategoryId2</i>).</td>
</tr>
<tr>
<td>Greater than zero </td>
<td>The first item should follow the second (<i>dwCategoryId1</i> &gt; <i>dwCategoryId2</i>).</td>
</tr>
<tr>
<td>Zero </td>
<td>The two items are the same (<i>dwCategoryId1</i> = <i>dwCategoryId2</i>).</td>
</tr>
</table>
 





