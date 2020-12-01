---
UID: NS:iads.ads_search_column
title: ADS_SEARCH_COLUMN (iads.h)
description: The ADS_SEARCH_COLUMN structure specifies the contents of a search column in the query returned from the directory service database.
helpviewer_keywords: ["*PADS_SEARCH_COLUMN","ADS_SEARCH_COLUMN","ADS_SEARCH_COLUMN structure [ADSI]","PADS_SEARCH_COLUMN","PADS_SEARCH_COLUMN structure pointer [ADSI]","_ds_ads_search_column","adsi.ads__search__column","adsi.ads_search_column","iads/ADS_SEARCH_COLUMN","iads/PADS_SEARCH_COLUMN"]
old-location: adsi\ads_search_column.htm
tech.root: adsi
ms.assetid: 9fdb370d-9409-4717-ae10-bb3b5b8a0e02
ms.date: 12/05/2018
ms.keywords: '*PADS_SEARCH_COLUMN, ADS_SEARCH_COLUMN, ADS_SEARCH_COLUMN structure [ADSI], PADS_SEARCH_COLUMN, PADS_SEARCH_COLUMN structure pointer [ADSI], _ds_ads_search_column, adsi.ads__search__column, adsi.ads_search_column, iads/ADS_SEARCH_COLUMN, iads/PADS_SEARCH_COLUMN'
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
targetos: Windows
req.typenames: ADS_SEARCH_COLUMN, *PADS_SEARCH_COLUMN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ads_search_column
 - iads/ads_search_column
 - PADS_SEARCH_COLUMN
 - iads/PADS_SEARCH_COLUMN
 - ADS_SEARCH_COLUMN
 - iads/ADS_SEARCH_COLUMN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SEARCH_COLUMN
---

# ADS_SEARCH_COLUMN structure


## -description

The <b>ADS_SEARCH_COLUMN</b> structure specifies the contents of a search column in the query returned from the directory service database.

## -struct-fields

### -field pszAttrName

A  null-terminated Unicode string that contains the name of the attribute whose values are contained in the current search column.

### -field dwADsType

Value from the  <a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a> enumeration that indicates how the attribute values are interpreted.

### -field pADsValues

Array of  <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structures that contain values of the attribute in the current search column for the current row.

### -field dwNumValues

Size of the <b>pADsValues</b> array.

### -field hReserved

Reserved for internal use by providers.

## -remarks

The <b>ADS_SEARCH_COLUMN</b> structure only contains a pointer to the array of  <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structures. Memory for the structure must be allocated separately.

For more information about  <b>ADS_SEARCH_COLUMN</b>, see  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">IDirectorySearch::GetColumn</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>



<a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a>



<a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">IDirectorySearch::GetColumn</a>