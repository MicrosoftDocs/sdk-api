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

# IClassFactory2::GetLicInfo


## -description


Retrieves information about the licensing capabilities of this class factory.


## -parameters




### -param pLicInfo [in, out]

A pointer to the caller-allocated <a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a> structure to be filled on output.


## -returns



This method can return the standard return values E_UNEXPECTED, as well as the following values.

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
The <a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a> structure was successfully filled in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pLicInfo</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not allowed as a return value because this method provides critical information for the client of a licensed class factory.




## -see-also




<a href="https://msdn.microsoft.com/c49c7612-3b1f-4535-baf3-8458b3f34f95">IClassFactory2</a>



<a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a>
 

 

