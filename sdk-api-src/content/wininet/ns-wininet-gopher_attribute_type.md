---
UID: NS:wininet.GOPHER_ATTRIBUTE_TYPE
title: GOPHER_ATTRIBUTE_TYPE (wininet.h)
description: Contains the relevant information of a single Gopher attribute for an object.
helpviewer_keywords: ["*LPGOPHER_ATTRIBUTE_TYPE","GOPHER_ATTRIBUTE_ID_ABSTRACT","GOPHER_ATTRIBUTE_ID_ADMIN","GOPHER_ATTRIBUTE_ID_GEOG","GOPHER_ATTRIBUTE_ID_LOCATION","GOPHER_ATTRIBUTE_ID_MOD_DATE","GOPHER_ATTRIBUTE_ID_ORG","GOPHER_ATTRIBUTE_ID_PROVIDER","GOPHER_ATTRIBUTE_ID_RANGE","GOPHER_ATTRIBUTE_ID_SCORE","GOPHER_ATTRIBUTE_ID_SITE","GOPHER_ATTRIBUTE_ID_TIMEZONE","GOPHER_ATTRIBUTE_ID_TREEWALK","GOPHER_ATTRIBUTE_ID_TTL","GOPHER_ATTRIBUTE_ID_UNKNOWN","GOPHER_ATTRIBUTE_ID_VERSION","GOPHER_ATTRIBUTE_ID_VIEW","GOPHER_ATTRIBUTE_TYPE","GOPHER_ATTRIBUTE_TYPE structure [WinINet]","GOPHER_CATEGORY_ID_ABSTRACT","GOPHER_CATEGORY_ID_ADMIN","GOPHER_CATEGORY_ID_ALL","GOPHER_CATEGORY_ID_INFO","GOPHER_CATEGORY_ID_UNKNOWN","GOPHER_CATEGORY_ID_VERONICA","GOPHER_CATEGORY_ID_VIEWS","LPGOPHER_ATTRIBUTE_TYPE","LPGOPHER_ATTRIBUTE_TYPE structure pointer [WinINet]","_win32_gopher_attribute_type","wininet.gopher_attribute_type","wininet/GOPHER_ATTRIBUTE_TYPE","wininet/LPGOPHER_ATTRIBUTE_TYPE"]
old-location: wininet\gopher_attribute_type.htm
tech.root: wininet
ms.assetid: 01daae8c-9080-4a8d-9f73-3e364ca868fe
ms.date: 12/05/2018
ms.keywords: '*LPGOPHER_ATTRIBUTE_TYPE, GOPHER_ATTRIBUTE_ID_ABSTRACT, GOPHER_ATTRIBUTE_ID_ADMIN, GOPHER_ATTRIBUTE_ID_GEOG, GOPHER_ATTRIBUTE_ID_LOCATION, GOPHER_ATTRIBUTE_ID_MOD_DATE, GOPHER_ATTRIBUTE_ID_ORG, GOPHER_ATTRIBUTE_ID_PROVIDER, GOPHER_ATTRIBUTE_ID_RANGE, GOPHER_ATTRIBUTE_ID_SCORE, GOPHER_ATTRIBUTE_ID_SITE, GOPHER_ATTRIBUTE_ID_TIMEZONE, GOPHER_ATTRIBUTE_ID_TREEWALK, GOPHER_ATTRIBUTE_ID_TTL, GOPHER_ATTRIBUTE_ID_UNKNOWN, GOPHER_ATTRIBUTE_ID_VERSION, GOPHER_ATTRIBUTE_ID_VIEW, GOPHER_ATTRIBUTE_TYPE, GOPHER_ATTRIBUTE_TYPE structure [WinINet], GOPHER_CATEGORY_ID_ABSTRACT, GOPHER_CATEGORY_ID_ADMIN, GOPHER_CATEGORY_ID_ALL, GOPHER_CATEGORY_ID_INFO, GOPHER_CATEGORY_ID_UNKNOWN, GOPHER_CATEGORY_ID_VERONICA, GOPHER_CATEGORY_ID_VIEWS, LPGOPHER_ATTRIBUTE_TYPE, LPGOPHER_ATTRIBUTE_TYPE structure pointer [WinINet], _win32_gopher_attribute_type, wininet.gopher_attribute_type, wininet/GOPHER_ATTRIBUTE_TYPE, wininet/LPGOPHER_ATTRIBUTE_TYPE'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: GOPHER_ATTRIBUTE_TYPE, *LPGOPHER_ATTRIBUTE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPGOPHER_ATTRIBUTE_TYPE
 - wininet/LPGOPHER_ATTRIBUTE_TYPE
 - GOPHER_ATTRIBUTE_TYPE
 - wininet/GOPHER_ATTRIBUTE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - GOPHER_ATTRIBUTE_TYPE
---

# GOPHER_ATTRIBUTE_TYPE structure


## -description

<p class="CCE_Message">[The <b>GOPHER_ATTRIBUTE_TYPE</b> structure is available for use in the operating systems specified in the Requirements section.]

Contains the relevant information of a single Gopher attribute for an object.

## -struct-fields

### -field CategoryId

Name of the Gopher category for the attribute. The possible values include: 

<a id="GOPHER_CATEGORY_ID_ABSTRACT"></a>
<a id="gopher_category_id_abstract"></a>


#### GOPHER_CATEGORY_ID_ABSTRACT

<a id="GOPHER_CATEGORY_ID_ADMIN"></a>
<a id="gopher_category_id_admin"></a>


#### GOPHER_CATEGORY_ID_ADMIN

<a id="GOPHER_CATEGORY_ID_ALL"></a>
<a id="gopher_category_id_all"></a>


#### GOPHER_CATEGORY_ID_ALL

<a id="GOPHER_CATEGORY_ID_INFO"></a>
<a id="gopher_category_id_info"></a>


#### GOPHER_CATEGORY_ID_INFO

<a id="GOPHER_CATEGORY_ID_UNKNOWN"></a>
<a id="gopher_category_id_unknown"></a>


#### GOPHER_CATEGORY_ID_UNKNOWN

<a id="GOPHER_CATEGORY_ID_VERONICA"></a>
<a id="gopher_category_id_veronica"></a>


#### GOPHER_CATEGORY_ID_VERONICA

<a id="GOPHER_CATEGORY_ID_VIEWS"></a>
<a id="gopher_category_id_views"></a>


#### GOPHER_CATEGORY_ID_VIEWS

### -field AttributeId

Attribute type. The possible values include: 

<a id="GOPHER_ATTRIBUTE_ID_ABSTRACT"></a>
<a id="gopher_attribute_id_abstract"></a>


#### GOPHER_ATTRIBUTE_ID_ABSTRACT

<a id="GOPHER_ATTRIBUTE_ID_ADMIN"></a>
<a id="gopher_attribute_id_admin"></a>


#### GOPHER_ATTRIBUTE_ID_ADMIN

<a id="GOPHER_ATTRIBUTE_ID_GEOG"></a>
<a id="gopher_attribute_id_geog"></a>


#### GOPHER_ATTRIBUTE_ID_GEOG

<a id="GOPHER_ATTRIBUTE_ID_LOCATION"></a>
<a id="gopher_attribute_id_location"></a>


#### GOPHER_ATTRIBUTE_ID_LOCATION

<a id="GOPHER_ATTRIBUTE_ID_MOD_DATE"></a>
<a id="gopher_attribute_id_mod_date"></a>


#### GOPHER_ATTRIBUTE_ID_MOD_DATE

<a id="GOPHER_ATTRIBUTE_ID_ORG"></a>
<a id="gopher_attribute_id_org"></a>


#### GOPHER_ATTRIBUTE_ID_ORG

<a id="GOPHER_ATTRIBUTE_ID_PROVIDER"></a>
<a id="gopher_attribute_id_provider"></a>


#### GOPHER_ATTRIBUTE_ID_PROVIDER

<a id="GOPHER_ATTRIBUTE_ID_RANGE"></a>
<a id="gopher_attribute_id_range"></a>


#### GOPHER_ATTRIBUTE_ID_RANGE

<a id="GOPHER_ATTRIBUTE_ID_SCORE"></a>
<a id="gopher_attribute_id_score"></a>


#### GOPHER_ATTRIBUTE_ID_SCORE

<a id="GOPHER_ATTRIBUTE_ID_SITE"></a>
<a id="gopher_attribute_id_site"></a>


#### GOPHER_ATTRIBUTE_ID_SITE

<a id="GOPHER_ATTRIBUTE_ID_TIMEZONE"></a>
<a id="gopher_attribute_id_timezone"></a>


#### GOPHER_ATTRIBUTE_ID_TIMEZONE

<a id="GOPHER_ATTRIBUTE_ID_TREEWALK"></a>
<a id="gopher_attribute_id_treewalk"></a>


#### GOPHER_ATTRIBUTE_ID_TREEWALK

<a id="GOPHER_ATTRIBUTE_ID_TTL"></a>
<a id="gopher_attribute_id_ttl"></a>


#### GOPHER_ATTRIBUTE_ID_TTL

<a id="GOPHER_ATTRIBUTE_ID_UNKNOWN"></a>
<a id="gopher_attribute_id_unknown"></a>


#### GOPHER_ATTRIBUTE_ID_UNKNOWN

<a id="GOPHER_ATTRIBUTE_ID_VERSION"></a>
<a id="gopher_attribute_id_version"></a>


#### GOPHER_ATTRIBUTE_ID_VERSION

<a id="GOPHER_ATTRIBUTE_ID_VIEW"></a>
<a id="gopher_attribute_id_view"></a>


#### GOPHER_ATTRIBUTE_ID_VIEW

### -field AttributeType

 Data for the Gopher attribute. The specific structure depends on the 
<b>AttributeId</b> member. The definitions of these data structures are available in Wininet.h. 



#### Admin

A <b>GOPHER_ADMIN_ATTRIBUTE</b> structure.



#### ModDate

A <b>GOPHER_MOD_DATE_ATTRIBUTE</b> structure.



#### Score

A <b>GOPHER_SCORE_ATTRIBUTE</b> structure.



#### ScoreRange

A <b>GOPHER_SCORE_RANGE_ATTRIBUTE</b> structure.



#### Site

A <b>GOPHER_SITE_ATTRIBUTE</b> structure.



#### Organization

A <b>GOPHER_ORGANIZATION_ATTRIBUTE</b> structure.



#### Location

A <b>GOPHER_LOCATION_ATTRIBUTE</b> structure.



#### GeographicalLocation

A <b>GOPHER_GEOGRAPHICAL_LOCATION_ATTRIBUTE</b> structure.



#### TimeZone

A <b>GOPHER_TIMEZONE_ATTRIBUTE</b> structure.



#### Provider

A <b>GOPHER_PROVIDER_ATTRIBUTE</b> structure.



#### Version

A <b>GOPHER_VERSION_ATTRIBUTE</b> structure.



#### Abstract

A <b>GOPHER_ABSTRACT_ATTRIBUTE</b> structure.



#### View

A <b>GOPHER_VIEW_ATTRIBUTE</b> structure.



#### Veronica

A <b>GOPHER_VERONICA_ATTRIBUTE</b> structure.



#### Ask

A <b>GOPHER_ASK_ATTRIBUTE_TYPE</b> structure.



#### Unknown

A <b>GOPHER_UNKNOWN_ATTRIBUTE</b> structure.

### -field Admin

### -field ModDate

### -field Ttl

### -field Score

### -field ScoreRange

### -field Site

### -field Organization

### -field Location

### -field GeographicalLocation

### -field TimeZone

### -field Provider

### -field Version

### -field Abstract

### -field View

### -field Veronica

### -field Ask

### -field Unknown

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nc-wininet-gopher_attribute_enumerator">GopherAttributeEnumerator</a>



<a href="/windows/desktop/api/wininet/nf-wininet-gophergetattributea">GopherGetAttribute</a>

