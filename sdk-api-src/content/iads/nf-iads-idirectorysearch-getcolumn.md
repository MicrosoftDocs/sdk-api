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

# IDirectorySearch::GetColumn


## -description


The <b>IDirectorySearch::GetColumn</b> method gets data from a named column of the search result.


## -parameters




### -param hSearchResult




### -param szColumnName [in]

Provides the name of the column for which data is requested.


### -param pSearchColumn [out]

Provides the address of a method-allocated  <a href="https://msdn.microsoft.com/9fdb370d-9409-4717-ae10-bb3b5b8a0e02">ADS_SEARCH_COLUMN</a> structure that contains the column from the current row of the search result.


#### - hSearchHandle [in]

Provides a handle to the search context.


## -returns



This method returns the standard return values, as well as the following.

For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The method allocates the memory for the  <a href="https://msdn.microsoft.com/9fdb370d-9409-4717-ae10-bb3b5b8a0e02">ADS_SEARCH_COLUMN</a> structure to hold the data of the column. But the caller must free the memory by calling  <a href="https://msdn.microsoft.com/72e75429-d22c-490f-a1f7-d771628067c9">IDirectorySearch::FreeColumn</a>.

The <b>IDirectorySearch::GetColumn</b> method tries to read the schema definition of the requested attribute so it can return the attribute values in the appropriate format in the <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures, contained in the <a href="https://msdn.microsoft.com/9fdb370d-9409-4717-ae10-bb3b5b8a0e02">ADS_SEARCH_COLUMN</a> structure. However, <b>GetColumn</b> can succeed even when the schema definition is not available, in which case the <b>dwADsType</b> member of the <b>ADS_SEARCH_COLUMN</b> structure returns ADSTYPE_PROV_SPECIFIC and the value is returned in an <a href="https://msdn.microsoft.com/45927280-7fb5-49a6-8ecd-f0a6931bed6a">ADS_PROV_SPECIFIC</a> structure. When you process the results of a <b>GetColumn</b> call, you must verify <b>dwADsType</b> to ensure that the data was returned in the expected format.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ADS_SEARCH_COLUMN col;
/*.. Omit the set preference and execute*/
while( m_pSearch-&gt;GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
{
   // Get the Name and display it in the list.
   hr = m_pSearch-&gt;GetColumn( hSearch, pszAttr[0], &amp;col );
   if ( SUCCEEDED(hr) )
   {
          switch (col.dwADsType)
          {
             case ADSTYPE_CASE_IGNORE_STRING:
                printf("%S\n", col.pADsValues-&gt;CaseIgnoreString);
             break;
 
             case ADSTYPE_PROV_SPECIFIC:
                printf("%S\n", col.pADsValues--&gt;ProviderSpecific.lpValue);
             break;
 
             default:
                printf("Unexpected ADsType: %d\n", col.dwADsType);
             break;
          }

          {
       
             m_pSearch-&gt;FreeColumn( &amp;col );
          }
   }
m_pSearch-&gt;CloseSearchHandle( hSearch );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/9fdb370d-9409-4717-ae10-bb3b5b8a0e02">ADS_SEARCH_COLUMN</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>



<a href="https://msdn.microsoft.com/72e75429-d22c-490f-a1f7-d771628067c9">IDirectorySearch::FreeColumn</a>
 

 

