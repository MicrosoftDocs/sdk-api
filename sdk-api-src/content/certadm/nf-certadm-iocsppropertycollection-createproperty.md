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

# IOCSPPropertyCollection::CreateProperty


## -description


The <b>CreateProperty</b> method creates a new property and adds it to a property set.


## -parameters




### -param bstrPropName [in]

A string that contains the name of the new property object.


### -param pVarPropValue [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>A pointer to the new property object.</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>The new property object.</td>
</tr>
</table>

### -param ppVal [out]

A pointer to an <a href="https://msdn.microsoft.com/854848f0-ea89-4c25-a8a5-40f1e4d229be">IOCSPProperty</a> interface for the newly created object.


## -returns



<h3>C++</h3>
If the method succeeds, it returns <b>S_OK</b>.


If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



<h3>VB</h3>
An 
<a href="https://msdn.microsoft.com/854848f0-ea89-4c25-a8a5-40f1e4d229be">IOCSPProperty</a>
 interface for the newly created object.



## -see-also




<a href="https://msdn.microsoft.com/8c700357-0cb4-4780-9ff1-ac57c46f9183">IOCSPPropertyCollection</a>
 

 

