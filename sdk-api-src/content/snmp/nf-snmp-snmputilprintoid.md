---
UID: NF:snmp.SnmpUtilPrintOid
title: SnmpUtilPrintOid function
author: windows-sdk-content
description: The SnmpUtilPrintOid function formats the specified object identifier (OID) and prints the result to the standard output device. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilprintoid.htm
tech.root: SNMP
ms.assetid: 8d5e9b79-83a5-49ed-8621-f12cbf9c59d0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SnmpUtilPrintOid, SnmpUtilPrintOid function [SNMP], _snmp_snmputilprintoid, snmp.snmputilprintoid, snmp/SnmpUtilPrintOid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SnmpUtilPrintOid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilPrintOid function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilPrintOid</b> function formats the specified object identifier (OID) and prints the result to the standard output device. This function is an element of the SNMP Utility API.


## -parameters




### -param Oid [in]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to print.


## -returns



This function does not return a value.




## -remarks



The 
<b>SnmpUtilPrintOid</b> function can assist with the debugging of command-line SNMP applications. The function prints the object identifier as a sequence of numbers separated by periods ('.'); for example, 1.3.6.1.4.1.311.




## -see-also




<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/ab092155-192f-450f-9635-9c34a4f572aa">SnmpUtilDbgPrint</a>
 

 

