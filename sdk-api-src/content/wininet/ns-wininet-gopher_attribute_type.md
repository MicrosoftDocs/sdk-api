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


### -field AttributeType.Admin

A <b>GOPHER_ADMIN_ATTRIBUTE</b> structure.


### -field AttributeType.ModDate

A <b>GOPHER_MOD_DATE_ATTRIBUTE</b> structure.


### -field AttributeType.Ttl

 


### -field AttributeType.Score

A <b>GOPHER_SCORE_ATTRIBUTE</b> structure.


### -field AttributeType.ScoreRange

A <b>GOPHER_SCORE_RANGE_ATTRIBUTE</b> structure.


### -field AttributeType.Site

A <b>GOPHER_SITE_ATTRIBUTE</b> structure.


### -field AttributeType.Organization

A <b>GOPHER_ORGANIZATION_ATTRIBUTE</b> structure.


### -field AttributeType.Location

A <b>GOPHER_LOCATION_ATTRIBUTE</b> structure.


### -field AttributeType.GeographicalLocation

A <b>GOPHER_GEOGRAPHICAL_LOCATION_ATTRIBUTE</b> structure.


### -field AttributeType.TimeZone

A <b>GOPHER_TIMEZONE_ATTRIBUTE</b> structure.


### -field AttributeType.Provider

A <b>GOPHER_PROVIDER_ATTRIBUTE</b> structure.


### -field AttributeType.Version

A <b>GOPHER_VERSION_ATTRIBUTE</b> structure.


### -field AttributeType.Abstract

A <b>GOPHER_ABSTRACT_ATTRIBUTE</b> structure.


### -field AttributeType.View

A <b>GOPHER_VIEW_ATTRIBUTE</b> structure.


### -field AttributeType.Veronica

A <b>GOPHER_VERONICA_ATTRIBUTE</b> structure.


### -field AttributeType.Ask

A <b>GOPHER_ASK_ATTRIBUTE_TYPE</b> structure.


### -field AttributeType.Unknown

A <b>GOPHER_UNKNOWN_ATTRIBUTE</b> structure.


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1a319d79-7866-4121-a80f-22e3bf983a0a">GopherAttributeEnumerator</a>



<a href="https://msdn.microsoft.com/c9e95532-8c65-45fb-acd0-a1f09cee2ce2">GopherGetAttribute</a>
 

 

