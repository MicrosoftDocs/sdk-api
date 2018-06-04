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

# EndUpdateResourceW function


## -description


Commits or discards changes made prior to a call to <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a>.


## -parameters




### -param hUpdate [in]

Type: <b>HANDLE</b>

A module handle returned by the <a href="https://msdn.microsoft.com/7702a24d-b786-47ae-9d7e-d047fbb50a7e">BeginUpdateResource</a> function, and used by <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a>, referencing the file to be updated. 


### -param fDiscard [in]

Type: <b>BOOL</b>

Indicates whether to write the resource updates to the file. If this parameter is <b>TRUE</b>, no changes are made. If it is <b>FALSE</b>, the changes are made: the resource updates will take effect. 


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the function succeeds; <b>FALSE</b> otherwise. If the function succeeds and 

<i>fDiscard</i> is <b>TRUE</b>, then no resource updates are made to the file; otherwise all 

successful resource updates are made to the file. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Before you call this function, make sure all file handles other than the one returned by <a href="https://msdn.microsoft.com/7702a24d-b786-47ae-9d7e-d047fbb50a7e">BeginUpdateResource</a> are closed.

This function can update resources within modules that contain both code and resources. There are restrictions on resource updates in LN files and .mui files, both of which contain Resource Configuration data; details of the restrictions are in the reference for the <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a> function.


#### Examples

For an example, see <a href="using_resources.htm">Updating Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7702a24d-b786-47ae-9d7e-d047fbb50a7e">BeginUpdateResource</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>



<a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a>
 

 

