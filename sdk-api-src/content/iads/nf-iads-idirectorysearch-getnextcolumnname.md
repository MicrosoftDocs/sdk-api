---
UID: NF:iads.IDirectorySearch.GetNextColumnName
title: IDirectorySearch::GetNextColumnName (iads.h)
description: The IDirectorySearch::GetNextColumnName method gets the name of the next column in the search result that contains data.
helpviewer_keywords: ["GetNextColumnName","GetNextColumnName method [ADSI]","GetNextColumnName method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","GetNextColumnName method","IDirectorySearch.GetNextColumnName","IDirectorySearch::GetNextColumnName","_ds_idirectorysearch_getnextcolumnname","adsi.idirectorysearch__getnextcolumnname","adsi.idirectorysearch_getnextcolumnname","iads/IDirectorySearch::GetNextColumnName"]
old-location: adsi\idirectorysearch_getnextcolumnname.htm
tech.root: adsi
ms.assetid: e3d95cc6-02f0-4a51-8dc5-4007cc8c63c8
ms.date: 12/05/2018
ms.keywords: GetNextColumnName, GetNextColumnName method [ADSI], GetNextColumnName method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetNextColumnName method, IDirectorySearch.GetNextColumnName, IDirectorySearch::GetNextColumnName, _ds_idirectorysearch_getnextcolumnname, adsi.idirectorysearch__getnextcolumnname, adsi.idirectorysearch_getnextcolumnname, iads/IDirectorySearch::GetNextColumnName
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
 - IDirectorySearch::GetNextColumnName
 - iads/IDirectorySearch::GetNextColumnName
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
 - IDirectorySearch.GetNextColumnName
---

# IDirectorySearch::GetNextColumnName


## -description

The <b>IDirectorySearch::GetNextColumnName</b> method gets the name of the next column in the search result that contains data.

## -parameters

### -param hSearchHandle [in]

Provides a handle to the search context.

### -param ppszColumnName [out]

Provides the address of a pointer to a method-allocated string containing the requested column name. If <b>NULL</b>, no subsequent rows contain data.

## -returns

This method returns the standard return values, as well as the following:

For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

This method allocates sufficient memory for the column name, but the caller must call the  <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a> helper function to free this memory when it is no longer needed.


#### Examples


```cpp
LPWSTR pszColumn;
m_pSearch->GetFirstRow( hSearch );
printf("Column names are: ");
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   printf("%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>