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

# ads_searchpref_info structure


## -description


The <b>ADS_SEARCHPREF_INFO</b> structure specifies the query preferences.


## -struct-fields




### -field dwSearchPref

Contains one of the  <a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a> enumeration values that specifies the search option to set.


### -field vValue

Contains a <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structure that specifies the data type and value of the search preference.


### -field dwStatus

Receives one of the  <a href="https://msdn.microsoft.com/dfc080da-f849-4df3-9b14-1193b9303742">ADS_STATUSENUM</a> enumeration values that indicates the status of the search preference. The <a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">IDirectorySearch::SetSearchPreference</a> method will fill in this member when it is called.


## -remarks



To setup a search preference, assign appropriate values to the fields of an  <b>ADS_SEARCHPREF_INFO</b> structure passed to the server. The <b>vValue</b> member of the <b>ADS_SEARCHPREF_INFO</b> structure is an <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structure. The following table lists the <a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a> values, the corresponding values for the <b>dwType</b> member of the <b>ADSVALUE</b> structure, and the <b>ADSVALUE</b> member that is used for the specified type.

<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a> Value</th>
<th><b>dwType</b> member of <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a>
</th>
<th>
<a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> member</th>
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
 

For more information and examples of how to use the <b>ADS_SEARCHPREF_INFO</b> structure, see the discussions of the  <a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">IDirectorySearch::SetSearchPreference</a> method and the  <a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a>



<a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a>



<a href="https://msdn.microsoft.com/dfc080da-f849-4df3-9b14-1193b9303742">ADS_STATUSENUM</a>



<a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">IDirectorySearch::SetSearchPreference</a>
 

 

