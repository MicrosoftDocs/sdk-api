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

# IMFProtectedEnvironmentAccess::Call


## -description


Allows content protection systems to access the protected environment.


## -parameters




### -param inputLength

The length in bytes of the input data.


### -param input

A pointer to the input data.


### -param outputLength

The length in bytes of the output data.


### -param output

A pointer to the output data.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



See  <a href="https://msdn.microsoft.com/B16BEFFD-26CF-4598-96A4-098C3E3AA51C">MFCreateProtectedEnvironmentAccess</a> for an example of how to create an <a href="https://msdn.microsoft.com/2cd93bc9-4a42-4e16-80aa-4ecf5900f5e4">IMFProtectedEnvironmentAccess</a> object and use the <b>Call</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2cd93bc9-4a42-4e16-80aa-4ecf5900f5e4">IMFProtectedEnvironmentAccess</a>



<a href="https://msdn.microsoft.com/B16BEFFD-26CF-4598-96A4-098C3E3AA51C">MFCreateProtectedEnvironmentAccess</a>
 

 

