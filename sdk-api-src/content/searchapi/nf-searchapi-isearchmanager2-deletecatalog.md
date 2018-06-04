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

# ISearchManager2::DeleteCatalog


## -description


Deletes an existing catalog and all associated indexed data from the Windows Search indexer.


## -parameters




### -param pszCatalog [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Name of catalog to delete. The catalog must at some prior time have been created with a call to CreateCatalog().


## -returns



Type: <b>HRESULT</b>

HRESULT indicating status of operation:

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
Catalog previously existed and has now been successfully deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Catalog did not previously existed, no change.

</td>
</tr>
</table>
 

FAILED HRESULT: Failure deleting catalog or invalid arguments passed.




## -see-also




<a href="https://msdn.microsoft.com/EE08AC43-D2E9-4B70-BBA5-52E36DD7F9A1">ISearchManager2</a>
 

 

