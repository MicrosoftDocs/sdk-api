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

# IWMPMediaCollection2::createQuery


## -description



The <b>createQuery</b> method retrieves a pointer to an <b>IWMPQuery</b> interface that represents a new query.




## -parameters




### -param ppQuery [out]

Address of a variable that receives an <b>IWMPQuery</b> pointer to the new, empty query.


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



Creating a new query is the first step toward creating a compound query.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/576e231e-542a-495c-ad1b-a246339c3cb1">IWMPMediaCollection2 Interface</a>



<a href="https://msdn.microsoft.com/f1f3c46f-4756-49b4-ad4f-a9097ff787f8">IWMPQuery Interface</a>
 

 

