---
UID: NS:winsnmp.smiVENDORINFO
title: smiVENDORINFO (winsnmp.h)
description: The smiVENDORINFO structure contains information about the Microsoft WinSNMP implementation.
helpviewer_keywords: ["*smiLPVENDORINFO","_snmp_smivendorinfo_str","smiLPVENDORINFO","smiLPVENDORINFO structure pointer [SNMP]","smiVENDORINFO","smiVENDORINFO structure [SNMP]","snmp.smivendorinfo_str","winsnmp/smiLPVENDORINFO","winsnmp/smiVENDORINFO"]
old-location: snmp\smivendorinfo_str.htm
tech.root: SNMP
ms.assetid: 78b7b736-f68a-456a-9178-9a5b40e3bc8d
ms.date: 12/05/2018
ms.keywords: '*smiLPVENDORINFO, _snmp_smivendorinfo_str, smiLPVENDORINFO, smiLPVENDORINFO structure pointer [SNMP], smiVENDORINFO, smiVENDORINFO structure [SNMP], snmp.smivendorinfo_str, winsnmp/smiLPVENDORINFO, winsnmp/smiVENDORINFO'
req.header: winsnmp.h
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
req.typenames: smiVENDORINFO, *smiLPVENDORINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - smiLPVENDORINFO
 - winsnmp/smiLPVENDORINFO
 - smiVENDORINFO
 - winsnmp/smiVENDORINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsnmp.h
api_name:
 - smiVENDORINFO
---

# smiVENDORINFO structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>smiVENDORINFO</b> structure contains information about the Microsoft WinSNMP implementation. A WinSNMP application can call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvendorinfo">SnmpGetVendorInfo</a> function to retrieve this structure. The 
<b>smiVENDORINFO</b> structure is an element of the WinSNMP API, version 2.0.

## -struct-fields

### -field vendorName

Contains the null-terminated string "Microsoft Corporation". The string is suitable for display to end users.

### -field vendorContact

Specifies a null-terminated character string that indicates how Microsoft can be contacted for WinSNMP-related information. For example, this member can contain a postal address, a telephone number or a fax number, a URL, or an e-mail address such as "snmpinfo@microsoft.com". The string is suitable for display.

### -field vendorVersionId

Specifies a null-terminated character string that identifies the version number of the WinSNMP API the Microsoft WinSNMP implementation is currently supporting. The string is suitable for display.

### -field vendorVersionDate

Specifies a null-terminated character string that indicates the release date of the version of the WinSNMP API the Microsoft WinSNMP implementation is currently supporting. The string is suitable for display.

### -field vendorEnterprise

Contains the value 311, Microsoft's enterprise number (permanent address) assigned by the Internet Assigned Numbers Authority (IANA).

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvendorinfo">SnmpGetVendorInfo</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/SNMP/winsnmp-structures">WinSNMP Structures</a>

