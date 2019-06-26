---
UID: NF:snmp.SnmpUtilAsnAnyFree
title: SnmpUtilAsnAnyFree function (snmp.h)
author: windows-sdk-content
description: The SnmpUtilAsnAnyFree function frees the memory allocated for the specified AsnAny structure. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilasnanyfree.htm
tech.root: SNMP
ms.assetid: b18c3722-398e-4659-ab1c-edd09d5c220d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpUtilAsnAnyFree, SnmpUtilAsnAnyFree function [SNMP], _snmp_snmputilasnanyfree, snmp.snmputilasnanyfree, snmp/SnmpUtilAsnAnyFree
ms.topic: function
f1_keywords: 
 - "snmp/SnmpUtilAsnAnyFree"
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
 - SnmpUtilAsnAnyFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpUtilAsnAnyFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
<b>SnmpUtilAsnAnyFree</b> function frees the memory allocated for the specified 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a> structure. This function is an element of the SNMP Utility API.


## -parameters




### -param pAny [in]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a> structure whose memory should be freed.


## -returns



This function does not return a value.




## -remarks



Call the 
<b>SnmpUtilAsnAnyFree</b> function to free the memory that the 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/nf-snmp-snmputilasnanycpy">SnmpUtilAsnAnyCpy</a> function allocates.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/snmp/nf-snmp-snmputilasnanycpy">SnmpUtilAsnAnyCpy</a>
 

 

