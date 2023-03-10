---
UID: NE:winnls.SYSGEOTYPE
title: SYSGEOTYPE (winnls.h)
description: Defines the type of geographical location information requested in the GetGeoInfo or GetGeoInfoEx function.
helpviewer_keywords: ["GEO_CURRENCYCODE","GEO_CURRENCYSYMBOL","GEO_DIALINGCODE","GEO_FRIENDLYNAME","GEO_ID","GEO_ISO2","GEO_ISO3","GEO_ISO_UN_NUMBER","GEO_LATITUDE","GEO_LCID","GEO_LONGITUDE","GEO_NAME","GEO_NATION","GEO_OFFICIALLANGUAGES","GEO_OFFICIALNAME","GEO_PARENT","GEO_RFC1766","GEO_TIMEZONES","SYSGEOTYPE","SYSGEOTYPE enumeration [Internationalization for Windows Applications]","_win32_SYSGEOTYPE","intl.sysgeotype","winnls/GEO_CURRENCYCODE","winnls/GEO_CURRENCYSYMBOL","winnls/GEO_DIALINGCODE","winnls/GEO_FRIENDLYNAME","winnls/GEO_ID","winnls/GEO_ISO2","winnls/GEO_ISO3","winnls/GEO_ISO_UN_NUMBER","winnls/GEO_LATITUDE","winnls/GEO_LCID","winnls/GEO_LONGITUDE","winnls/GEO_NAME","winnls/GEO_NATION","winnls/GEO_OFFICIALLANGUAGES","winnls/GEO_OFFICIALNAME","winnls/GEO_PARENT","winnls/GEO_RFC1766","winnls/GEO_TIMEZONES","winnls/SYSGEOTYPE"]
old-location: intl\sysgeotype.htm
tech.root: Intl
ms.assetid: f72f5cc5-4709-408f-a50c-b4b3092c4419
ms.date: 12/05/2018
ms.keywords: GEO_CURRENCYCODE, GEO_CURRENCYSYMBOL, GEO_DIALINGCODE, GEO_FRIENDLYNAME, GEO_ID, GEO_ISO2, GEO_ISO3, GEO_ISO_UN_NUMBER, GEO_LATITUDE, GEO_LCID, GEO_LONGITUDE, GEO_NAME, GEO_NATION, GEO_OFFICIALLANGUAGES, GEO_OFFICIALNAME, GEO_PARENT, GEO_RFC1766, GEO_TIMEZONES, SYSGEOTYPE, SYSGEOTYPE enumeration [Internationalization for Windows Applications], _win32_SYSGEOTYPE, intl.sysgeotype, winnls/GEO_CURRENCYCODE, winnls/GEO_CURRENCYSYMBOL, winnls/GEO_DIALINGCODE, winnls/GEO_FRIENDLYNAME, winnls/GEO_ID, winnls/GEO_ISO2, winnls/GEO_ISO3, winnls/GEO_ISO_UN_NUMBER, winnls/GEO_LATITUDE, winnls/GEO_LCID, winnls/GEO_LONGITUDE, winnls/GEO_NAME, winnls/GEO_NATION, winnls/GEO_OFFICIALLANGUAGES, winnls/GEO_OFFICIALNAME, winnls/GEO_PARENT, winnls/GEO_RFC1766, winnls/GEO_TIMEZONES, winnls/SYSGEOTYPE
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYSGEOTYPE
 - winnls/SYSGEOTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - SYSGEOTYPE
---

# SYSGEOTYPE enumeration


## -description

Defines the type of geographical location information requested in the <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoa">GetGeoInfo</a> or <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoex">GetGeoInfoEx</a> function.

## -enum-fields

### -field GEO_NATION:0x0001

The geographical location identifier (GEOID) of a nation. This value is stored in a long integer.

<b>Starting with Windows 10, version 1709:</b> This value is not supported for the <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoex">GetGeoInfoEx</a> function, and should not be used.

### -field GEO_LATITUDE:0x0002

The latitude of the location. This value is stored in a floating-point number.

### -field GEO_LONGITUDE:0x0003

The longitude of the location. This value is stored in a floating-point number.

### -field GEO_ISO2:0x0004

The ISO 2-letter country/region code. This value is stored in a string.

### -field GEO_ISO3:0x0005

The ISO 3-letter country/region code. This value is stored in a string.

### -field GEO_RFC1766:0x0006

The name for a string, compliant with RFC 4646 (starting with Windows Vista), that is derived from the <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoa">GetGeoInfo</a> parameters <i>language</i> and <i>GeoId</i>.

<b>Starting with Windows 10, version 1709:</b> This value is not supported for the <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoex">GetGeoInfoEx</a> function, and should not be used.

### -field GEO_LCID:0x0007

A locale identifier derived using <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoa">GetGeoInfo</a>.

<b>Starting with Windows 10, version 1709:</b> This value is not supported for the <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoex">GetGeoInfoEx</a> function, and should not be used.

### -field GEO_FRIENDLYNAME:0x0008

The friendly name of the nation, for example, Germany. This value is stored in a string.

### -field GEO_OFFICIALNAME:0x0009

The official name of the nation, for example, Federal Republic of Germany. This value is stored in a string.

### -field GEO_TIMEZONES:0x000A

Not implemented.

### -field GEO_OFFICIALLANGUAGES:0x000B

Not implemented.

### -field GEO_ISO_UN_NUMBER:0x000C

<b>Starting with Windows 8:</b> The ISO 3-digit country/region code. This value is stored in a string.

### -field GEO_PARENT:0x000D

<b>Starting with Windows 8:</b> The geographical location identifier of the parent region of a country/region. This value is stored in a string.

### -field GEO_DIALINGCODE:0x000E

<b>Starting with Windows 10, version 1709:</b> The dialing code to use with telephone numbers in the geographic location.  For example, 1 for the United States.

### -field GEO_CURRENCYCODE:0x000F

<b>Starting with Windows 10, version 1709:</b> The three-letter code for the currency that the geographic location uses.  For example, USD for United States dollars.

### -field GEO_CURRENCYSYMBOL:0x0010

<b>Starting with Windows 10, version 1709:</b> The symbol for the currency that the geographic location uses.  For example, the dollar sign ($).

### -field GEO_NAME:0x0011

<b>Starting with Windows 10, version 1709:</b> The two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code for the geographic region.

For information about two-letter ISO 3166-1 codes, see <a href="https://www.iso.org/iso-3166-country-codes.html">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://unstats.un.org/unsd/methodology/m49/">Standard country or area codes for statistical use (M49)</a>.

### -field GEO_ID:0x0012  

<b>Starting with Windows 10, version 1709:</b> The Windows geographical location identifiers (GEOID) for the region. This value is provided for backward compatibility.  Do not use this value in new applications, but use <b>GEO_NAME</b> instead.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoa">GetGeoInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoex">GetGeoInfoEx</a>



<a href="/windows/desktop/Intl/national-language-support-enumeration-types">National Language Support Enumeration Types</a>
