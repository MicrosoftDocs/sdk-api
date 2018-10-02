---
UID: NF:snmp.SnmpUtilAsnAnyFree
title: SnmpUtilAsnAnyFree function
author: windows-sdk-content
description: The SnmpUtilAsnAnyFree function frees the memory allocated for the specified AsnAny structure. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilasnanyfree.htm
tech.root: SNMP
ms.assetid: b18c3722-398e-4659-ab1c-edd09d5c220d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SnmpUtilAsnAnyFree, SnmpUtilAsnAnyFree function [SNMP], _snmp_snmputilasnanyfree, snmp.snmputilasnanyfree, snmp/SnmpUtilAsnAnyFree
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
 - SnmpUtilAsnAnyFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilAsnAnyFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
<b>SnmpUtilAsnAnyFree</b> function frees the memory allocated for the specified 
<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a> structure. This function is an element of the SNMP Utility API.


## -parameters




### -param pAny [in]

Pointer to an 
<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a> structure whose memory should be freed.


## -returns



This function does not return a value.




## -remarks



Call the 
<b>SnmpUtilAsnAnyFree</b> function to free the memory that the 
<a href="https://msdn.microsoft.com/0a8743da-ef4a-4b00-b9be-5550896d147a">SnmpUtilAsnAnyCpy</a> function allocates.




## -see-also




<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/0a8743da-ef4a-4b00-b9be-5550896d147a">SnmpUtilAsnAnyCpy</a>
 

 

