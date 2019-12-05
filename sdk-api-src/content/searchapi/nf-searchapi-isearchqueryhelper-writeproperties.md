---
UID: NF:searchapi.ISearchQueryHelper.WriteProperties
title: ISearchQueryHelper::WriteProperties (searchapi.h)
description: Not implemented.
old-location: search\_search_ISearchQueryHelper_WriteProperties.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\writeproperties.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],WriteProperties method, ISearchQueryHelper.WriteProperties, ISearchQueryHelper::WriteProperties, WriteProperties, WriteProperties method [search], WriteProperties method [search],ISearchQueryHelper interface, _search_ISearchQueryHelper_WriteProperties, search._search_ISearchQueryHelper_WriteProperties, searchapi/ISearchQueryHelper::WriteProperties
ms.topic: method
f1_keywords:
- searchapi/ISearchQueryHelper.WriteProperties
dev_langs:
- c++
req.header: searchapi.h
req.include-header: Searchapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
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
- ISearchQueryHelper.WriteProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchQueryHelper::WriteProperties


## -description


Not implemented.


## -parameters




### -param itemID [in]

Type: <b>int</b>

The ItemID that is to be affected. The ItemID is used to store the items unique identifier, such as a DocID.


### -param dwNumberOfColumns [in]

Type: <b>DWORD</b>

The number of properties being written.


### -param pColumns [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

 
                Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures that represent the properties.


### -param pValues [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ns-searchapi-search_column_properties">SEARCH_COLUMN_PROPERTIES</a>*</b>

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ns-searchapi-search_column_properties">SEARCH_COLUMN_PROPERTIES</a> structures that hold the property values.


### -param pftGatherModifiedTime [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>*</b>

A pointer to the last modified time for the item being written. This time stamp is used later to see if an item has been changed and requires updating.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties">ISearchQueryHelper::put_QueryContentProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>



<a href="https://msdn.microsoft.com/library/ff518152(v=VS.85).aspx">System Properties</a>
 

 

