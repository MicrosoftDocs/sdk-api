---
UID: NF:snmp.SnmpUtilOidFree
title: SnmpUtilOidFree function (snmp.h)
author: windows-sdk-content
description: The SnmpUtilOidFree function frees the memory allocated for the specified object identifier. This function is an element of the SNMP Utility API.
old-location: snmp\snmputiloidfree.htm
tech.root: SNMP
ms.assetid: 8fc44fdf-956a-4102-bcbb-4cd17a73828c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpUtilOidFree, SnmpUtilOidFree function [SNMP], _snmp_snmputiloidfree, snmp.snmputiloidfree, snmp/SnmpUtilOidFree
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
 - SnmpUtilOidFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpUtilOidFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidFree</b> function frees the memory allocated for the specified object identifier. This function is an element of the SNMP Utility API.


## -parameters




### -param pOid [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure whose memory should be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/8ffa5638-13ef-4cec-80f0-303611a52dac">SnmpUtilOidAppend</a>
 

 

