---
UID: NF:iads.IDirectorySearch.GetNextColumnName
title: IDirectorySearch::GetNextColumnName
author: windows-sdk-content
description: The IDirectorySearch::GetNextColumnName method gets the name of the next column in the search result that contains data.
old-location: adsi\idirectorysearch_getnextcolumnname.htm
old-project: ADSI
ms.assetid: e3d95cc6-02f0-4a51-8dc5-4007cc8c63c8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetNextColumnName, GetNextColumnName method [ADSI], GetNextColumnName method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetNextColumnName method, IDirectorySearch.GetNextColumnName, IDirectorySearch::GetNextColumnName, _ds_idirectorysearch_getnextcolumnname, adsi.idirectorysearch__getnextcolumnname, adsi.idirectorysearch_getnextcolumnname, iads/IDirectorySearch::GetNextColumnName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
req.product: GDI+ 1.1
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

For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



This method allocates sufficient memory for the column name, but the caller must call the  <a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a> helper function to free this memory when it is no longer needed.


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




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>
 

 

