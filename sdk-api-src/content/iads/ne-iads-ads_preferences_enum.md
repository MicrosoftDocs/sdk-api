---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0022
title: ADS_PREFERENCES_ENUM (iads.h)
description: The ADS_PREFERENCES_ENUM enumeration specifies the query preferences of the OLE DB provider for ADSI.
helpviewer_keywords: ["ADSIPROP_ADSIFLAG","ADSIPROP_ASYNCHRONOUS","ADSIPROP_ATTRIBTYPES_ONLY","ADSIPROP_CACHE_RESULTS","ADSIPROP_CHASE_REFERRALS","ADSIPROP_DEREF_ALIASES","ADSIPROP_PAGED_TIME_LIMIT","ADSIPROP_PAGESIZE","ADSIPROP_SEARCH_SCOPE","ADSIPROP_SIZE_LIMIT","ADSIPROP_SORT_ON","ADSIPROP_TIMEOUT","ADSIPROP_TIME_LIMIT","ADS_PREFERENCES_ENUM","ADS_PREFERENCES_ENUM enumeration [ADSI]","_ds_ads_preferences_enum","adsi.ads__preferences__enum","adsi.ads_preferences_enum","iads/ADSIPROP_ADSIFLAG","iads/ADSIPROP_ASYNCHRONOUS","iads/ADSIPROP_ATTRIBTYPES_ONLY","iads/ADSIPROP_CACHE_RESULTS","iads/ADSIPROP_CHASE_REFERRALS","iads/ADSIPROP_DEREF_ALIASES","iads/ADSIPROP_PAGED_TIME_LIMIT","iads/ADSIPROP_PAGESIZE","iads/ADSIPROP_SEARCH_SCOPE","iads/ADSIPROP_SIZE_LIMIT","iads/ADSIPROP_SORT_ON","iads/ADSIPROP_TIMEOUT","iads/ADSIPROP_TIME_LIMIT","iads/ADS_PREFERENCES_ENUM"]
old-location: adsi\ads_preferences_enum.htm
tech.root: adsi
ms.assetid: 9a6e3235-b7a6-4f63-910c-0d286b3be018
ms.date: 12/05/2018
ms.keywords: ADSIPROP_ADSIFLAG, ADSIPROP_ASYNCHRONOUS, ADSIPROP_ATTRIBTYPES_ONLY, ADSIPROP_CACHE_RESULTS, ADSIPROP_CHASE_REFERRALS, ADSIPROP_DEREF_ALIASES, ADSIPROP_PAGED_TIME_LIMIT, ADSIPROP_PAGESIZE, ADSIPROP_SEARCH_SCOPE, ADSIPROP_SIZE_LIMIT, ADSIPROP_SORT_ON, ADSIPROP_TIMEOUT, ADSIPROP_TIME_LIMIT, ADS_PREFERENCES_ENUM, ADS_PREFERENCES_ENUM enumeration [ADSI], _ds_ads_preferences_enum, adsi.ads__preferences__enum, adsi.ads_preferences_enum, iads/ADSIPROP_ADSIFLAG, iads/ADSIPROP_ASYNCHRONOUS, iads/ADSIPROP_ATTRIBTYPES_ONLY, iads/ADSIPROP_CACHE_RESULTS, iads/ADSIPROP_CHASE_REFERRALS, iads/ADSIPROP_DEREF_ALIASES, iads/ADSIPROP_PAGED_TIME_LIMIT, iads/ADSIPROP_PAGESIZE, iads/ADSIPROP_SEARCH_SCOPE, iads/ADSIPROP_SIZE_LIMIT, iads/ADSIPROP_SORT_ON, iads/ADSIPROP_TIMEOUT, iads/ADSIPROP_TIME_LIMIT, iads/ADS_PREFERENCES_ENUM
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
req.typenames: ADS_PREFERENCES_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0022
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0022
 - ADS_PREFERENCES_ENUM
 - iads/ADS_PREFERENCES_ENUM
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
 - ADS_PREFERENCES_ENUM
---

# ADS_PREFERENCES_ENUM enumeration


## -description

The <b>ADS_PREFERENCES_ENUM</b> enumeration specifies the query preferences of the OLE DB provider for ADSI.

## -enum-fields

### -field ADSIPROP_ASYNCHRONOUS:0

Requests an asynchronous search.

### -field ADSIPROP_DEREF_ALIASES:0x1

Specifies that aliases of found objects are to be resolved. Use  <a href="/windows/win32/api/iads/ne-iads-ads_derefenum">ADS_DEREFENUM</a> to specify how to perform this operation.

### -field ADSIPROP_SIZE_LIMIT:0x2

Specifies the size limit that the server should observe in a search. The size limit is the maximum number of returned objects. A zero value indicates that no size limit is imposed. The server stops searching once the size limit is reached and returns the results accumulated up to that point.

### -field ADSIPROP_TIME_LIMIT:0x3

Specifies the time limit, in seconds, that the server should observe in a search. A zero value indicates that no time limit restriction is imposed. When the time limit is reached, the server stops searching and returns  results  accumulated to that point.

### -field ADSIPROP_ATTRIBTYPES_ONLY:0x4

Indicates that the search should obtain only the name of attributes to which values have been assigned.

### -field ADSIPROP_SEARCH_SCOPE:0x5

Specifies the search scope that should be observed by the server. For more information about the appropriate settings, see the  <a href="/windows/win32/api/iads/ne-iads-ads_scopeenum">ADS_SCOPEENUM</a> enumeration.

### -field ADSIPROP_TIMEOUT:0x6

Specifies the time limit, in seconds, that a client will wait for the server to return the result.

### -field ADSIPROP_PAGESIZE:0x7

Specifies the page size in a paged search. For each request by the client, the server returns, at most, the number of objects as set by the page size.

### -field ADSIPROP_PAGED_TIME_LIMIT:0x8

Specifies the time limit, in seconds, that the server should observe to search a page of results; this is  opposed to the time limit for the entire search.

### -field ADSIPROP_CHASE_REFERRALS:0x9

Specifies that referrals may be chased. If the root search is not specified in the naming context of the server or when the search results cross a naming context (for example, when you have child domains and search in the parent domain), the server sends a referral message to the client which the client can choose to ignore or chase. By default, this option is set to ADS_CHASE_REFERRALS_EXTERNAL. For more information about referrals chasing, see  <a href="/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum">ADS_CHASE_REFERRALS_ENUM</a>.

### -field ADSIPROP_SORT_ON:0xa

Specifies that the server sorts the result set. Use the  <a href="/windows/desktop/api/iads/ns-iads-ads_sortkey">ADS_SORTKEY</a> structure to specify the sort keys.

### -field ADSIPROP_CACHE_RESULTS:0xb

Specifies if the result should be cached on the client side. By default, ADSI caches the result set. Turning off this option may be more desirable for large result sets.

### -field ADSIPROP_ADSIFLAG:0xc

Allows the OLEDB client to specify bind flags to use when binding to the server. Valid values are those allowed by  <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>. It is accessed from ADO scripts using the property name "ADSI Flag."

## -remarks

Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Instead, use the numerical constants to set the appropriate flags in your VBScript application. To use the symbolic constants, as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript application.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum">ADS_CHASE_REFERRALS_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_derefenum">ADS_DEREFENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_scopeenum">ADS_SCOPEENUM</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_sortkey">ADS_SORTKEY</a>
