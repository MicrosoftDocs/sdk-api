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

# CLSIDFromProgID function


## -description


Looks up a CLSID in the registry, given a ProgID.


## -parameters




### -param lpszProgID [in]

A pointer to the ProgID whose CLSID is requested.


### -param lpclsid [out]

Receives a pointer to the retrieved CLSID on return.


## -returns



This function can return the following values.

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
The CLSID was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
The registered CLSID for the ProgID is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_WRITEREGDB</b></dt>
</dl>
</td>
<td width="60%">
An error occurred writing the CLSID to the registry. See Remarks below.


</td>
</tr>
</table>
 




## -remarks



Given a ProgID, <b>CLSIDFromProgID</b> looks up its associated CLSID in the registry. If the ProgID cannot be found in the registry, <b>CLSIDFromProgID</b> creates an OLE 1 CLSID for the ProgID and a CLSID entry in the registry. Because of the restrictions placed on OLE 1 CLSID values, <b>CLSIDFromProgID</b> and <a href="https://msdn.microsoft.com/36cc9037-480f-491f-a9bb-5aa1e707781e">CLSIDFromString</a> are the only two functions that can be used to generate a CLSID for an OLE 1 object.




## -see-also




<a href="https://msdn.microsoft.com/2f937ac1-b214-482a-af4b-8cc8c0c585c3">CLSIDFromProgIDEx</a>



<a href="https://msdn.microsoft.com/a863cbc2-f8ab-468a-8254-b273077a6a2b">ProgIDFromCLSID</a>
 

 

