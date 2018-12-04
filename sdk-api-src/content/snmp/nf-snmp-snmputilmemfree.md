---
UID: NF:snmp.SnmpUtilMemFree
title: SnmpUtilMemFree function
author: windows-sdk-content
description: The SnmpUtilMemFree function frees the specified memory object. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilmemfree.htm
tech.root: SNMP
ms.assetid: 57cf0398-d2c1-4dd9-ad77-0c453412034a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SnmpUtilMemFree, SnmpUtilMemFree function [SNMP], _snmp_snmputilmemfree, snmp.snmputilmemfree, snmp/SnmpUtilMemFree
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
 - SnmpUtilMemFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilMemFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilMemFree</b> function frees the specified memory object. This function is an element of the SNMP Utility API.


## -parameters




### -param pMem [in, out]

Pointer to the memory object to release.


## -returns



This function does not return a value.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/85e293da-4c5b-4b32-9b86-e63074d37274">SnmpUtilMemAlloc</a> function to allocate the memory for the object.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/85e293da-4c5b-4b32-9b86-e63074d37274">SnmpUtilMemAlloc</a>



<a href="https://msdn.microsoft.com/269b6f57-cdef-476a-bf38-f35535d15999">SnmpUtilMemReAlloc</a>
 

 

