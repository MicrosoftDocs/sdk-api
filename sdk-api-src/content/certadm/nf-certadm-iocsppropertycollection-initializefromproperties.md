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

# IOCSPPropertyCollection::InitializeFromProperties


## -description


The <b>InitializeFromProperties</b> method creates a property set from the properties contained in an existing server configuration.


## -parameters




### -param pVarProperties [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
A pointer to an array that contains the property values. Each array element is a <b>VARIANT</b> array that contains the property name <b>BSTR</b> and a value <b>VARIANT</b>.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
An array that contains the property values. Each array element is a <b>Variant</b> array that contains the property name <b>String</b> and a value <b>Variant</b>.

</td>
</tr>
</table>

## -returns



<h3>VB</h3>
If the method succeeds, it returns <b>S_OK</b>.


If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

If the method returns <b>E_UNEXPECTED</b>, the array pointed to by the <i>pVarProperties</i> parameter contained duplicate properties.

If the method returns <b>DISP_E_ARRAYISLOCKED</b>, the array pointed to by the <i>pVarProperties</i> parameter is locked.




## -see-also




<a href="https://msdn.microsoft.com/8c700357-0cb4-4780-9ff1-ac57c46f9183">IOCSPPropertyCollection</a>
 

 

