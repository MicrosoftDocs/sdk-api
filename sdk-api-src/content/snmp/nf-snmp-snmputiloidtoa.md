---
UID: NF:snmp.SnmpUtilOidToA
title: SnmpUtilOidToA function
author: windows-sdk-content
description: The SnmpUtilOidToA function converts an object identifier (OID) to a null-terminated string. This function is an element of the SNMP Utility API.
old-location: snmp\snmputiloidtoa.htm
old-project: SNMP
ms.assetid: c21124ac-f2f8-4096-9100-639ded42d198
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SnmpUtilOidToA, SnmpUtilOidToA function [SNMP], _snmp_snmputiloidtoa, snmp.snmputiloidtoa, snmp/SnmpUtilOidToA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: snmp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilOidToA
product: Windows
targetos: Windows
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpUtilOidToA function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidToA</b> function converts an object identifier (OID) to a null-terminated string. This function is an element of the SNMP Utility API.


## -parameters




### -param Oid [in]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to convert.


## -returns



The function returns a null-terminated string of characters that contains the string representation of the object identifier pointed to by the <i>Oid</i> parameter.




## -remarks



The 
<b>SnmpUtilOidToA</b> function can assist with the debugging of SNMP applications.

For more information, see the 
<a href="https://msdn.microsoft.com/0a8e1ead-a1f8-4aeb-ae89-d9b135ccbb14">SnmpUtilIdsToA</a> function. 
<b>SnmpUtilOidToA</b> calls 
<b>SnmpUtilIdsToA</b> internally to format the string.




## -see-also




<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/0a8e1ead-a1f8-4aeb-ae89-d9b135ccbb14">SnmpUtilIdsToA</a>
 

 

