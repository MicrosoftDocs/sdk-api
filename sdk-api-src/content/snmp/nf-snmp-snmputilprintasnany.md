---
UID: NF:snmp.SnmpUtilPrintAsnAny
title: SnmpUtilPrintAsnAny function (snmp.h)
author: windows-sdk-content
description: The SnmpUtilPrintAsnAny function prints the value of the Any parameter to the standard output. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilprintasnany.htm
tech.root: SNMP
ms.assetid: 2dd52131-defb-4613-a889-a115d60a969a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpUtilPrintAsnAny, SnmpUtilPrintAsnAny function [SNMP], _snmp_snmputilprintasnany, snmp.snmputilprintasnany, snmp/SnmpUtilPrintAsnAny
ms.topic: function
f1_keywords: 
 - "snmp/SnmpUtilPrintAsnAny"
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
 - SnmpUtilPrintAsnAny
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpUtilPrintAsnAny function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilPrintAsnAny</b> function prints the value of the <i>Any</i> parameter to the standard output. This function is an element of the SNMP Utility API.


## -parameters




### -param pAny [in]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a> structure for a value to print.


## -returns



This function does not return a value.




## -remarks



Use the 
<b>SnmpUtilPrintAsnAny</b> function for debugging and development purposes. This function does not generally print the data in a form that a manager application would typically need.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>
 

 

