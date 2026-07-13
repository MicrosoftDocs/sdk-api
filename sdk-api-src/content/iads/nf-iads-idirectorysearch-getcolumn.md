---
UID: NF:iads.IDirectorySearch.GetColumn
title: IDirectorySearch::GetColumn (iads.h)
description: The IDirectorySearch::GetColumn method gets data from a named column of the search result.
helpviewer_keywords: ["GetColumn","GetColumn method [ADSI]","GetColumn method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","GetColumn method","IDirectorySearch.GetColumn","IDirectorySearch::GetColumn","_ds_idirectorysearch_getcolumn","adsi.idirectorysearch__getcolumn","adsi.idirectorysearch_getcolumn","iads/IDirectorySearch::GetColumn"]
old-location: adsi\idirectorysearch_getcolumn.htm
tech.root: adsi
ms.assetid: 3bcacb24-a4b4-4fad-ab7c-79ef7a67064d
ms.date: 12/05/2018
ms.keywords: GetColumn, GetColumn method [ADSI], GetColumn method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetColumn method, IDirectorySearch.GetColumn, IDirectorySearch::GetColumn, _ds_idirectorysearch_getcolumn, adsi.idirectorysearch__getcolumn, adsi.idirectorysearch_getcolumn, iads/IDirectorySearch::GetColumn
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectorySearch::GetColumn
 - iads/IDirectorySearch::GetColumn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
 - Adsldp.dll
 - Adsldpc.dll
api_name:
 - IDirectorySearch.GetColumn
---

# IDirectorySearch::GetColumn


## -description

The <b>IDirectorySearch::GetColumn</b> method gets data from a named column of the search result.

## -parameters

### -param hSearchResult [in]

Provides a handle to the search context.

### -param szColumnName [in]

Provides the name of the column for which data is requested.

### -param pSearchColumn [out]

Provides the address of a method-allocated  <a href="/windows/desktop/api/iads/ns-iads-ads_search_column">ADS_SEARCH_COLUMN</a> structure that contains the column from the current row of the search result.

## -returns

This method returns the standard return values, as well as the following.

For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The method allocates the memory for the  <a href="/windows/desktop/api/iads/ns-iads-ads_search_column">ADS_SEARCH_COLUMN</a> structure to hold the data of the column. But the caller must free the memory by calling  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-freecolumn">IDirectorySearch::FreeColumn</a>.

The <b>IDirectorySearch::GetColumn</b> method tries to read the schema definition of the requested attribute so it can return the attribute values in the appropriate format in the <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structures, contained in the <a href="/windows/desktop/api/iads/ns-iads-ads_search_column">ADS_SEARCH_COLUMN</a> structure. However, <b>GetColumn</b> can succeed even when the schema definition is not available, in which case the <b>dwADsType</b> member of the <b>ADS_SEARCH_COLUMN</b> structure returns ADSTYPE_PROV_SPECIFIC and the value is returned in an <a href="/windows/win32/api/iads/ns-iads-ads_prov_specific">ADS_PROV_SPECIFIC</a> structure. When you process the results of a <b>GetColumn</b> call, you must verify <b>dwADsType</b> to ensure that the data was returned in the expected format.


#### Examples


```cpp
ADS_SEARCH_COLUMN col;
/*.. Omit the set preference and execute*/
while( m_pSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
{
   // Get the Name and display it in the list.
   hr = m_pSearch->GetColumn( hSearch, pszAttr[0], &col );
   if ( SUCCEEDED(hr) )
   {
          switch (col.dwADsType)
          {
             case ADSTYPE_CASE_IGNORE_STRING:
                printf("%S\n", col.pADsValues->CaseIgnoreString);
             break;
 
             case ADSTYPE_PROV_SPECIFIC:
                printf("%S\n", col.pADsValues->ProviderSpecific.lpValue);
             break;
 
             default:
                printf("Unexpected ADsType: %d\n", col.dwADsType);
             break;
          }

          {
             m_pSearch->FreeColumn( &col );
          }
   }

}

m_pSearch->CloseSearchHandle( hSearch );

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_search_column">ADS_SEARCH_COLUMN</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-freecolumn">IDirectorySearch::FreeColumn</a>
