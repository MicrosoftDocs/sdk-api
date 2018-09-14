---
UID: NE:winnls.SYSGEOTYPE
title: SYSGEOTYPE
author: windows-sdk-content
description: Defines the type of geographical location information requested in the GetGeoInfo or GetGeoInfoEx function.
old-location: intl\sysgeotype.htm
tech.root: Intl
ms.assetid: f72f5cc5-4709-408f-a50c-b4b3092c4419
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GEO_CURRENCYCODE, GEO_CURRENCYSYMBOL, GEO_DIALINGCODE, GEO_FRIENDLYNAME, GEO_ID, GEO_ISO2, GEO_ISO3, GEO_ISO_UN_NUMBER, GEO_LATITUDE, GEO_LCID, GEO_LONGITUDE, GEO_NAME, GEO_NATION, GEO_OFFICIALLANGUAGES, GEO_OFFICIALNAME, GEO_PARENT, GEO_RFC1766, GEO_TIMEZONES, SYSGEOTYPE, SYSGEOTYPE enumeration [Internationalization for Windows Applications], _win32_SYSGEOTYPE, intl.sysgeotype, winnls/GEO_CURRENCYCODE, winnls/GEO_CURRENCYSYMBOL, winnls/GEO_DIALINGCODE, winnls/GEO_FRIENDLYNAME, winnls/GEO_ID, winnls/GEO_ISO2, winnls/GEO_ISO3, winnls/GEO_ISO_UN_NUMBER, winnls/GEO_LATITUDE, winnls/GEO_LCID, winnls/GEO_LONGITUDE, winnls/GEO_NAME, winnls/GEO_NATION, winnls/GEO_OFFICIALLANGUAGES, winnls/GEO_OFFICIALNAME, winnls/GEO_PARENT, winnls/GEO_RFC1766, winnls/GEO_TIMEZONES, winnls/SYSGEOTYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - Winnls.h
api_name:
 - SYSGEOTYPE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SYSGEOTYPE enumeration


## -description


Defines the type of geographical location information requested in the <a href="https://msdn.microsoft.com/73827ed9-bdc5-4b34-b849-fb44b3c5bd6e">GetGeoInfo</a> or <a href="https://msdn.microsoft.com/05BF6434-A80F-4BF5-9A43-C4D65E72F43B">GetGeoInfoEx</a> function.


## -enum-fields




### -field GEO_NATION

The geographical location identifier (GEOID) of a nation. This value is stored in a long integer.

<b>Starting with Windows 10, version 1709:</b> This value is not supported for the <a href="https://msdn.microsoft.com/05BF6434-A80F-4BF5-9A43-C4D65E72F43B">GetGeoInfoEx</a> function, and should not be used.


### -field GEO_LATITUDE

The latitude of the location. This value is stored in a floating-point number.


### -field GEO_LONGITUDE

The longitude of the location. This value is stored in a floating-point number.


### -field GEO_ISO2

The ISO 2-letter country/region code. This value is stored in a string.


### -field GEO_ISO3

The ISO 3-letter country/region code. This value is stored in a string.


### -field GEO_RFC1766

The name for a string, compliant with RFC 4646 (starting with Windows Vista), that is derived from the <a href="https://msdn.microsoft.com/73827ed9-bdc5-4b34-b849-fb44b3c5bd6e">GetGeoInfo</a> parameters <i>language</i> and <i>GeoId</i>.

<b>Starting with Windows 10, version 1709:</b> This value is not supported for the <a href="https://msdn.microsoft.com/05BF6434-A80F-4BF5-9A43-C4D65E72F43B">GetGeoInfoEx</a> function, and should not be used.


### -field GEO_LCID

A locale identifier derived using <a href="https://msdn.microsoft.com/73827ed9-bdc5-4b34-b849-fb44b3c5bd6e">GetGeoInfo</a>.

<b>Starting with Windows 10, version 1709:</b> This value is not supported for the <a href="https://msdn.microsoft.com/05BF6434-A80F-4BF5-9A43-C4D65E72F43B">GetGeoInfoEx</a> function, and should not be used.


### -field GEO_FRIENDLYNAME

The friendly name of the nation, for example, Germany. This value is stored in a string.


### -field GEO_OFFICIALNAME

The official name of the nation, for example, Federal Republic of Germany. This value is stored in a string.


### -field GEO_TIMEZONES

Not implemented.


### -field GEO_OFFICIALLANGUAGES

Not implemented.


### -field GEO_ISO_UN_NUMBER

<b>Starting with Windows 8:</b> The ISO 3-digit country/region code. This value is stored in a string.


### -field GEO_PARENT

<b>Starting with Windows 8:</b> The geographical location identifier of the parent region of a country/region. This value is stored in a string.


### -field GEO_DIALINGCODE

<b>Starting with Windows 10, version 1709:</b> The dialing code to use with telephone numbers in the geographic location.  For example, 1 for the United States.


### -field GEO_CURRENCYCODE

<b>Starting with Windows 10, version 1709:</b> The three-letter code for the currency that the geographic location uses.  For example, USD for United States dollars.


### -field GEO_CURRENCYSYMBOL

<b>Starting with Windows 10, version 1709:</b> The symbol for the currency that the geographic location uses.  For example, the dollar sign ($).


### -field GEO_NAME

<b>Starting with Windows 10, version 1709:</b> The two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code for the geographic region.

For information about two-letter ISO 3166-1 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859039">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859018">Standard country or area codes for statistical use (M49)</a>.


### -field GEO_ID

<b>Starting with Windows 10, version 1709:</b> The Windows geographical location identifiers (GEOID) for the region. This value is provided for backward compatibility.  Do not use this value in new applications, but use <b>GEO_NAME</b> instead.


## -see-also




<a href="https://msdn.microsoft.com/73827ed9-bdc5-4b34-b849-fb44b3c5bd6e">GetGeoInfo</a>



<a href="https://msdn.microsoft.com/05BF6434-A80F-4BF5-9A43-C4D65E72F43B">GetGeoInfoEx</a>



<a href="https://msdn.microsoft.com/93911b65-e2ba-432d-9c65-53dd57687077">National Language Support Enumeration Types</a>
 

 

