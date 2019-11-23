---
UID: NF:snmp.SnmpUtilOctetsCmp
title: SnmpUtilOctetsCmp function (snmp.h)

description: The SnmpUtilOctetsCmp function compares two octet strings. This function is an element of the SNMP Utility API.
old-location: snmp\snmputiloctetscmp.htm
tech.root: SNMP
ms.assetid: b7d12b31-488c-4b0b-b803-516054c99c34

ms.date: 12/05/2018
ms.keywords: SnmpUtilOctetsCmp, SnmpUtilOctetsCmp function [SNMP], _snmp_snmputiloctetscmp, snmp.snmputiloctetscmp, snmp/SnmpUtilOctetsCmp
ms.topic: function
f1_keywords: 
 - "snmp/SnmpUtilOctetsCmp"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilOctetsCmp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpUtilOctetsCmp function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOctetsCmp</b> function compares two octet strings. This function is an element of the SNMP Utility API.


## -parameters




### -param pOctets1 [in]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a> structure to compare.


### -param pOctets2 [in]

Pointer to a second 
<b>AsnOctetString</b> structure to compare.


## -returns



The function returns a value greater than zero if <i>pOctets1</i> is greater than <i>pOctets2</i>, zero if <i>pOctets1</i> equals <i>pOctets2</i>, and less than zero if <i>pOctets1</i> is less than <i>pOctets2</i>.
						




## -remarks



The 
<b>SnmpUtilOctetsCmp</b> function calls the 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/nf-snmp-snmputiloctetsncmp">SnmpUtilOctetsNCmp</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/snmp/nf-snmp-snmputiloctetsncmp">SnmpUtilOctetsNCmp</a>
 

 

