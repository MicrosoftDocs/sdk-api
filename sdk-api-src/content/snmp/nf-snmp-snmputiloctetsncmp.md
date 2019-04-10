---
UID: NF:snmp.SnmpUtilOctetsNCmp
title: SnmpUtilOctetsNCmp function (snmp.h)
author: windows-sdk-content
description: The SnmpUtilOctetsNCmp function compares two octet strings. The function compares the subidentifiers in the strings until it reaches the number of subidentifiers specified by the nChars parameter. SnmpUtilOctetsNCmp is an element of the SNMP Utility API.
old-location: snmp\snmputiloctetsncmp.htm
tech.root: SNMP
ms.assetid: bba13c41-1c0f-4a54-9a93-8115ef77c086
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpUtilOctetsNCmp, SnmpUtilOctetsNCmp function [SNMP], _snmp_snmputiloctetsncmp, snmp.snmputiloctetsncmp, snmp/SnmpUtilOctetsNCmp
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
 - SnmpUtilOctetsNCmp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilOctetsNCmp function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOctetsNCmp</b> function compares two octet strings. The function compares the subidentifiers in the strings until it reaches the number of subidentifiers specified by the <i>nChars</i> parameter. 
<b>SnmpUtilOctetsNCmp</b> is an element of the SNMP Utility API.


## -parameters




### -param pOctets1 [in]

Pointer to an 
<a href="https://msdn.microsoft.com/d58c54e2-0479-408f-977d-63409e5f500e">AsnOctetString</a> structure to compare.


### -param pOctets2 [in]

Pointer to a second 
<b>AsnOctetString</b> structure to compare.


### -param nChars [in]

Specifies the number of subidentifiers to compare.


## -returns



The function returns a value greater than zero if <i>pOctets1</i> is greater than <i>pOctets2</i>, zero if <i>pOctets1</i> equals <i>pOctets2</i>, and less than zero if <i>pOctets1</i> is less than <i>pOctets2</i>.
						




## -remarks



The 
<a href="https://msdn.microsoft.com/b7d12b31-488c-4b0b-b803-516054c99c34">SnmpUtilOctetsCmp</a> function calls the 
<b>SnmpUtilOctetsNCmp</b> function.




## -see-also




<a href="https://msdn.microsoft.com/d58c54e2-0479-408f-977d-63409e5f500e">AsnOctetString</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/b7d12b31-488c-4b0b-b803-516054c99c34">SnmpUtilOctetsCmp</a>
 

 

