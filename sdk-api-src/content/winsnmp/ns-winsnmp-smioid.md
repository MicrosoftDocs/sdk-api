---
UID: NS:winsnmp.smiOID
title: smiOID (winsnmp.h)
description: The WinSNMP smiOID structure passes object identifiers to multiple WinSNMP functions. The structure also receives the variable name of a variable binding entry in a call to the SnmpGetVb function.
helpviewer_keywords: ["*smiLPOID","_snmp_smioid_str","smiLPOID","smiLPOID structure pointer [SNMP]","smiOID","smiOID structure [SNMP]","snmp.smioid_str","winsnmp/smiLPOID","winsnmp/smiOID"]
old-location: snmp\smioid_str.htm
tech.root: SNMP
ms.assetid: 0bdf900e-6e67-4461-97bc-4c9650d888bf
ms.date: 12/05/2018
ms.keywords: '*smiLPOID, _snmp_smioid_str, smiLPOID, smiLPOID structure pointer [SNMP], smiOID, smiOID structure [SNMP], snmp.smioid_str, winsnmp/smiLPOID, winsnmp/smiOID'
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
req.typenames: smiOID, *smiLPOID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - smiLPOID
 - winsnmp/smiLPOID
 - smiOID
 - winsnmp/smiOID
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
 - smiOID
---

# smiOID structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>smiOID</b> structure passes object identifiers to multiple WinSNMP functions. The structure also receives the variable name of a variable binding entry in a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvb">SnmpGetVb</a> function.

The 
<b>smiOID</b> structure contains a pointer to a variable length array of a named object's subidentifiers. The structure can be a member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a> structure.

## -struct-fields

### -field len

Specifies an unsigned long integer value that indicates the number of elements in the array pointed to by the <b>ptr</b> member.

### -field ptr

Pointer to an array of unsigned long integers that represent the object identifier's subidentifiers.

## -remarks

In an 
<b>smiOID</b> structure, the format of the array pointed to by the <b>ptr</b> member is one subidentifier per array element. For example, the string "1.3.6.1" would be an array of four elements {1,3,6,1}.

The Microsoft WinSNMP implementation allocates and deallocates memory for all output 
<b>smiOID</b> structures. The WinSNMP application should not free memory that the implementation allocates for the <b>ptr</b> member of an 
<b>smiOID</b> structure. Instead, the application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to free the memory.

Because the WinSNMP application allocates memory for input descriptor objects with variable lengths, it must free that memory. For more information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvb">SnmpGetVb</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpoidcompare">SnmpOidCompare</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpoidcopy">SnmpOidCopy</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpoidtostr">SnmpOidToStr</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtooid">SnmpStrToOid</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/SNMP/winsnmp-structures">WinSNMP Structures</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a>

