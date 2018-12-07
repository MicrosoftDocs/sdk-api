---
UID: NF:snmp.SnmpUtilOidCmp
title: SnmpUtilOidCmp function
author: windows-sdk-content
description: The SnmpUtilOidCmp function compares two object identifiers. This function is an element of the SNMP Utility API.
old-location: snmp\snmputiloidcmp.htm
tech.root: SNMP
ms.assetid: c6ec4984-d984-4642-b110-fd9c2c7e3c5d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpUtilOidCmp, SnmpUtilOidCmp function [SNMP], _snmp_snmputiloidcmp, snmp.snmputiloidcmp, snmp/SnmpUtilOidCmp
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
 - SnmpUtilOidCmp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilOidCmp function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidCmp</b> function compares two object identifiers. This function is an element of the SNMP Utility API.


## -parameters




### -param pOid1 [in]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to compare.


### -param pOid2 [in]

Pointer to a second 
<b>AsnObjectIdentifier</b> structure to compare.


## -returns



The function returns a value greater than zero if <i>pOid1</i> is greater than <i>pOid2</i>, zero if <i>pOid1</i> equals <i>pOid2</i>, and less than zero if <i>pOid1</i> is less than <i>pOid2</i>.




## -remarks



The 
<b>SnmpUtilOidCmp</b> function calls the 
<a href="https://msdn.microsoft.com/a23df516-9559-4209-bf2d-8268737d1dfb">SnmpUtilOidNCmp</a> function.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/a23df516-9559-4209-bf2d-8268737d1dfb">SnmpUtilOidNCmp</a>
 

 

