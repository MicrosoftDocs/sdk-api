---
UID: NS:iads.ads_search_column
title: ADS_SEARCH_COLUMN (iads.h)
author: windows-sdk-content
description: The ADS_SEARCH_COLUMN structure specifies the contents of a search column in the query returned from the directory service database.
old-location: adsi\ads_search_column.htm
tech.root: adsi
ms.assetid: 9fdb370d-9409-4717-ae10-bb3b5b8a0e02
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PADS_SEARCH_COLUMN, ADS_SEARCH_COLUMN, ADS_SEARCH_COLUMN structure [ADSI], PADS_SEARCH_COLUMN, PADS_SEARCH_COLUMN structure pointer [ADSI], _ds_ads_search_column, adsi.ads__search__column, adsi.ads_search_column, iads/ADS_SEARCH_COLUMN, iads/PADS_SEARCH_COLUMN"
ms.topic: struct
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SEARCH_COLUMN
product: Windows
targetos: Windows
req.typenames: ADS_SEARCH_COLUMN, *PADS_SEARCH_COLUMN
req.redist: 
---

# ADS_SEARCH_COLUMN structure


## -description


The <b>ADS_SEARCH_COLUMN</b> structure specifies the contents of a search column in the query returned from the directory service database.


## -struct-fields




### -field pszAttrName

A  null-terminated Unicode string that contains the name of the attribute whose values are contained in the current search column.


### -field dwADsType

Value from the  <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> enumeration that indicates how the attribute values are interpreted.


### -field pADsValues

Array of  <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures that contain values of the attribute in the current search column for the current row.


### -field dwNumValues

Size of the <b>pADsValues</b> array.


### -field hReserved

Reserved for internal use by providers.


## -remarks



The <b>ADS_SEARCH_COLUMN</b> structure only contains a pointer to the array of  <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures. Memory for the structure must be allocated separately.

For more information about  <b>ADS_SEARCH_COLUMN</b>, see  <a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">IDirectorySearch::GetColumn</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a>



<a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">IDirectorySearch::GetColumn</a>
 

 

