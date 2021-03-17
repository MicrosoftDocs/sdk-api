---
UID: NF:searchapi.ISearchManager2.DeleteCatalog
title: ISearchManager2::DeleteCatalog (searchapi.h)
description: Deletes an existing catalog and all associated indexed data from the Windows Search indexer.
helpviewer_keywords: ["DeleteCatalog","DeleteCatalog method [search]","DeleteCatalog method [search]","ISearchManager2 interface","ISearchManager2 interface [search]","DeleteCatalog method","ISearchManager2.DeleteCatalog","ISearchManager2::DeleteCatalog","search.isearchmanager2_deletecatalog","searchapi/ISearchManager2::DeleteCatalog"]
old-location: search\isearchmanager2_deletecatalog.htm
tech.root: search
ms.assetid: E9515AEE-6854-4FF8-9A83-10E6BC247D4D
ms.date: 12/05/2018
ms.keywords: DeleteCatalog, DeleteCatalog method [search], DeleteCatalog method [search],ISearchManager2 interface, ISearchManager2 interface [search],DeleteCatalog method, ISearchManager2.DeleteCatalog, ISearchManager2::DeleteCatalog, search.isearchmanager2_deletecatalog, searchapi/ISearchManager2::DeleteCatalog
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchManager2::DeleteCatalog
 - searchapi/ISearchManager2::DeleteCatalog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchManager2.DeleteCatalog
---

# ISearchManager2::DeleteCatalog


## -description

Deletes an existing catalog and all associated indexed data from the Windows Search indexer.

## -parameters

### -param pszCatalog [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

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

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2">ISearchManager2</a>