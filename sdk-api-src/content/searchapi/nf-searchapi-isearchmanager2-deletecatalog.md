---
UID: NF:searchapi.ISearchManager2.DeleteCatalog
title: ISearchManager2::DeleteCatalog
author: windows-sdk-content
description: Deletes an existing catalog and all associated indexed data from the Windows Search indexer.
old-location: search\isearchmanager2_deletecatalog.htm
old-project: search
ms.assetid: E9515AEE-6854-4FF8-9A83-10E6BC247D4D
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DeleteCatalog, DeleteCatalog method [search], DeleteCatalog method [search],ISearchManager2 interface, ISearchManager2 interface [search],DeleteCatalog method, ISearchManager2.DeleteCatalog, ISearchManager2::DeleteCatalog, search.isearchmanager2_deletecatalog, searchapi/ISearchManager2::DeleteCatalog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchManager2.DeleteCatalog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

