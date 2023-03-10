---
UID: NS:winsnmp.smiOCTETS
title: smiOCTETS (winsnmp.h)
description: The WinSNMP smiOCTETS structure passes context strings to multiple WinSNMP functions. The structure also describes and receives encoded SNMP messages.
helpviewer_keywords: ["*smiLPBITS","*smiLPIPADDR","*smiLPNSAPADDR","*smiLPOCTETS","*smiLPOPAQUE","_snmp_smioctets_str","smiBITS","smiIPADDR","smiLPOCTETS","smiLPOCTETS structure pointer [SNMP]","smiNSAPADDR","smiOCTETS","smiOCTETS structure [SNMP]","smiOPAQUE","snmp.smioctets_str","winsnmp/smiLPOCTETS","winsnmp/smiOCTETS"]
old-location: snmp\smioctets_str.htm
tech.root: SNMP
ms.assetid: d53da0e8-ce7d-4923-90c3-2469cbd9d9b1
ms.date: 12/05/2018
ms.keywords: '*smiLPBITS, *smiLPIPADDR, *smiLPNSAPADDR, *smiLPOCTETS, *smiLPOPAQUE, _snmp_smioctets_str, smiBITS, smiIPADDR, smiLPOCTETS, smiLPOCTETS structure pointer [SNMP], smiNSAPADDR, smiOCTETS, smiOCTETS structure [SNMP], smiOPAQUE, snmp.smioctets_str, winsnmp/smiLPOCTETS, winsnmp/smiOCTETS'
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
req.typenames: smiOCTETS, *smiLPOCTETS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - smiLPOCTETS
 - winsnmp/smiLPOCTETS
 - smiOCTETS
 - winsnmp/smiOCTETS
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
 - smiOCTETS
---

# smiOCTETS structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>smiOCTETS</b> structure passes context strings to multiple WinSNMP functions. The structure also describes and receives encoded SNMP messages.

The 
<b>smiOCTETS</b> structure contains a pointer to an SNMP octet string of variable length. The structure can be a member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a> structure.

## -struct-fields

### -field len

Specifies an unsigned long integer value that indicates the number of bytes in the octet string array pointed to by the <b>ptr</b> member.

### -field ptr

Pointer to a byte array that contains the octet string of interest. A <b>NULL</b>-terminating byte is not required.

## -remarks

The Microsoft WinSNMP implementation allocates and deallocates memory for all output 
<b>smiOCTETS</b> structures. The WinSNMP application should not free memory that the implementation allocates for the <b>ptr</b> member of an 
<b>smiOCTETS</b> structure. Instead, the application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to free the memory.

Because the WinSNMP application allocates memory for input descriptor objects with variable lengths, it must free that memory. For more information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcontexttostr">SnmpContextToStr</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpdecodemsg">SnmpDecodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtocontext">SnmpStrToContext</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/SNMP/winsnmp-structures">WinSNMP Structures</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a>

