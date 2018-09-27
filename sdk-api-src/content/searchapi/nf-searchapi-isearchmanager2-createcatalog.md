---
UID: NF:searchapi.ISearchManager2.CreateCatalog
title: ISearchManager2::CreateCatalog
author: windows-sdk-content
description: Creates a new custom catalog in the Windows Search indexer and returns a reference to it.
old-location: search\isearchmanager2_createcatalog.htm
tech.root: search
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: CreateCatalog, CreateCatalog method [search], CreateCatalog method [search],ISearchManager2 interface, ISearchManager2 interface [search],CreateCatalog method, ISearchManager2.CreateCatalog, ISearchManager2::CreateCatalog, search.isearchmanager2_createcatalog, searchapi/ISearchManager2::CreateCatalog
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchManager2.CreateCatalog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchManager2::CreateCatalog


## -description


Creates a new custom catalog in the Windows Search indexer and returns a reference to it.


## -parameters




### -param pszCatalog [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Name of catalog to create. Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.


### -param ppCatalogManager [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb266414(v=VS.85).aspx">ISearchCatalogManager</a>**</b>

On success a reference to the created catalog is returned as an <a href="https://msdn.microsoft.com/en-us/library/Bb266414(v=VS.85).aspx">ISearchCatalogManager</a> interface pointer. The Release() must be called on this interface after the calling application has finished using it.


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
Catalog did not previously exist and was created. Reference to catalog returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Catalog previously existed, reference to catalog returned.

</td>
</tr>
</table>
 

FAILED HRESULT: Failure creating catalog or invalid arguments passed.





## -remarks



Called to create a new catalog in the Windows Search indexer.
After creation, the methods on the returned  <a href="https://msdn.microsoft.com/en-us/library/Bb266414(v=VS.85).aspx">ISearchCatalog</a> manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.
See the â€œManaging the Indexâ€ documentation for more info: http://msdn.microsoft.com/en-us/library/bb266516(VS.85).aspx 





## -see-also




<a href="https://msdn.microsoft.com/EE08AC43-D2E9-4B70-BBA5-52E36DD7F9A1">ISearchManager2</a>
 

 

