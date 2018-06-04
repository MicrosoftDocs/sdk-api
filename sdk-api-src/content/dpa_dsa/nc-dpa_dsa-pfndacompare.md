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

# PFNDACOMPARE callback function


## -description


Defines the prototype for the compare function used by <a href="https://msdn.microsoft.com/cf9c56fd-eeca-414a-8c3f-a962d41b1161">DSA_Sort</a>.


## -parameters




### -param *p1 [in, optional]

Type: <b>void*</b>

A pointer to the first item in the comparison.


### -param *p2 [in, optional]

Type: <b>void*</b>

A pointer to the second item in the comparison.


### -param lParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Additional data passed to <i>pfnCmp</i>.


## -returns



Type: <b>int</b>

The meaning of the return values depends on the function that uses this callback prototype. The return values for <a href="https://msdn.microsoft.com/cf9c56fd-eeca-414a-8c3f-a962d41b1161">DSA_Sort</a> are the following.
                        
                        


<table class="clsStd">
<tr>
<td>less than 0</td>
<td>If <i>p1</i> should be sorted ahead of <i>p2</i>.</td>
</tr>
<tr>
<td>equal to 0</td>
<td>If <i>p1</i> and <i>p2</i> should be sorted together.</td>
</tr>
<tr>
<td>greater than 0</td>
<td>If <i>p1</i> should be sorted after <i>p2</i>.</td>
</tr>
</table>
 






## -remarks



Alternate names for this callback are <b>PFNDPACOMPARE</b> and <b>PFNDSACOMPARE</b>.



