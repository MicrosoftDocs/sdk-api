---
UID: NF:snmp.SnmpUtilIdsToA
title: SnmpUtilIdsToA function (snmp.h)
description: The SnmpUtilIdsToA function converts an object identifier (OID) to a null-terminated string. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilIdsToA","SnmpUtilIdsToA function [SNMP]","_snmp_snmputilidstoa","snmp.snmputilidstoa","snmp/SnmpUtilIdsToA"]
old-location: snmp\snmputilidstoa.htm
tech.root: SNMP
ms.assetid: 0a8e1ead-a1f8-4aeb-ae89-d9b135ccbb14
ms.date: 12/05/2018
ms.keywords: SnmpUtilIdsToA, SnmpUtilIdsToA function [SNMP], _snmp_snmputilidstoa, snmp.snmputilidstoa, snmp/SnmpUtilIdsToA
req.header: snmp.h
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
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpUtilIdsToA
 - snmp/SnmpUtilIdsToA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilIdsToA
---

# SnmpUtilIdsToA function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilIdsToA</b> function converts an object identifier (OID) to a null-terminated string. This function is an element of the SNMP Utility API.

## -parameters

### -param Ids [in]

Pointer to an array of unsigned integers. The array contains the sequence of numbers that the OID contains. The <i>IdLength</i> parameter specifies the array's length. 




For more information, see the following Return Values and Remarks sections.

### -param IdLength [in]

Specifies the number of elements in the array pointed to by the <i>Ids</i> parameter.

## -returns

The function returns a null-terminated string that contains the string representation of the array of numbers pointed to by the <i>Ids</i> parameter. The string contains a sequence of numbers separated by periods ('.'); for example, 1.3.6.1.4.1.311.

If the <i>Ids</i> parameter is null, or if the <i>IdLength</i> parameter specifies zero, the function returns the string "&lt;null oid&gt;".

The maximum length of the returned string is 256 characters. If the string's length exceeds 256 characters, the string is truncated and terminated with a sequence of three periods ('...').

## -remarks

The 
<b>SnmpUtilIdsToA</b> function can assist with the debugging of SNMP applications.

Note that the following memory restrictions apply when you call 
<b>SnmpUtilIdsToA</b>:

<ul>
<li>The <i>Ids</i> parameter must point to a valid memory block of at least <i>IdLength</i> integers, or the function call results in an access violation exception.</li>
<li>The string returned by 
<b>SnmpUtilIdsToA</b> resides in memory that the SNMP Utility API allocates. The application should not make any assumptions about the memory allocation. The data is guaranteed to be valid until you call 
<b>SnmpUtilIdsToA</b> again, so before calling the function again you should copy the data to another location.</li>
</ul>

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidtoa">SnmpUtilOidToA</a>