---
UID: NS:iads.ads_searchpref_info
title: ADS_SEARCHPREF_INFO (iads.h)
description: The ADS_SEARCHPREF_INFO structure specifies the query preferences.
helpviewer_keywords: ["*LPADS_SEARCHPREF_INFO","*PADS_SEARCHPREF_INFO","ADS_SEARCHPREF_INFO","ADS_SEARCHPREF_INFO structure [ADSI]","LPADS_SEARCHPREF_INFO","LPADS_SEARCHPREF_INFO structure pointer [ADSI]","PADS_SEARCHPREF_INFO","PADS_SEARCHPREF_INFO structure pointer [ADSI]","_ds_ads_searchpref_info","adsi.ads__searchpref__info","adsi.ads_searchpref_info","iads/ADS_SEARCHPREF_INFO","iads/LPADS_SEARCHPREF_INFO","iads/PADS_SEARCHPREF_INFO"]
old-location: adsi\ads_searchpref_info.htm
tech.root: adsi
ms.assetid: 5fc46271-a1be-4a9d-a340-ed801211736a
ms.date: 12/05/2018
ms.keywords: '*LPADS_SEARCHPREF_INFO, *PADS_SEARCHPREF_INFO, ADS_SEARCHPREF_INFO, ADS_SEARCHPREF_INFO structure [ADSI], LPADS_SEARCHPREF_INFO, LPADS_SEARCHPREF_INFO structure pointer [ADSI], PADS_SEARCHPREF_INFO, PADS_SEARCHPREF_INFO structure pointer [ADSI], _ds_ads_searchpref_info, adsi.ads__searchpref__info, adsi.ads_searchpref_info, iads/ADS_SEARCHPREF_INFO, iads/LPADS_SEARCHPREF_INFO, iads/PADS_SEARCHPREF_INFO'
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
req.typenames: ADS_SEARCHPREF_INFO, *PADS_SEARCHPREF_INFO, *LPADS_SEARCHPREF_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ads_searchpref_info
 - iads/ads_searchpref_info
 - PADS_SEARCHPREF_INFO
 - iads/PADS_SEARCHPREF_INFO
 - ADS_SEARCHPREF_INFO
 - iads/ADS_SEARCHPREF_INFO
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
 - ADS_SEARCHPREF_INFO
---

# ADS_SEARCHPREF_INFO structure


## -description

The <b>ADS_SEARCHPREF_INFO</b> structure specifies the query preferences.

## -struct-fields

### -field dwSearchPref

Contains one of the  <a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a> enumeration values that specifies the search option to set.

### -field vValue

Contains a <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure that specifies the data type and value of the search preference.

### -field dwStatus

Receives one of the  <a href="/windows/win32/api/iads/ne-iads-ads_statusenum">ADS_STATUSENUM</a> enumeration values that indicates the status of the search preference. The <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> method will fill in this member when it is called.

## -remarks

To setup a search preference, assign appropriate values to the fields of an  <b>ADS_SEARCHPREF_INFO</b> structure passed to the server. The <b>vValue</b> member of the <b>ADS_SEARCHPREF_INFO</b> structure is an <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure. The following table lists the <a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a> values, the corresponding values for the <b>dwType</b> member of the <b>ADSVALUE</b> structure, and the <b>ADSVALUE</b> member that is used for the specified type.

<table>
<tr>
<th>
<a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a> Value</th>
<th><b>dwType</b> member of <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a>
</th>
<th>
<a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> member</th>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_ASYNCHRONOUS</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_DEREF_ALIASES</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SIZE_LIMIT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_TIME_LIMIT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_ATTRIBTYPES_ONLY</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SEARCH_SCOPE</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_TIMEOUT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_PAGESIZE</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_PAGED_TIME_LIMIT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_CHASE_REFERRALS</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SORT_ON</b></td>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td><b>ProviderSpecific</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_CACHE_RESULTS</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_DIRSYNC</b></td>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td><b>ProviderSpecific</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_TOMBSTONE</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_VLV</b></td>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td><b>ProviderSpecific</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_ATTRIBUTE_QUERY</b></td>
<td><b>ADSTYPE_CASE_IGNORE_STRING</b></td>
<td><b>CaseIgnoreString</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SECURITY_MASK</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_DIRSYNC_FLAG</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_EXTENDED_DN</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
</table>
 

For more information and examples of how to use the <b>ADS_SEARCHPREF_INFO</b> structure, see the discussions of the  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> method and the  <a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a> enumeration.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>



<a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a>



<a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_statusenum">ADS_STATUSENUM</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a>