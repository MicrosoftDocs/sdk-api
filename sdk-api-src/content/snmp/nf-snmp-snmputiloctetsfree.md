---
UID: NF:snmp.SnmpUtilOctetsFree
title: SnmpUtilOctetsFree function
author: windows-sdk-content
description: The SnmpUtilOctetsFree function frees the memory allocated for the specified octet string. This function is an element of the SNMP Utility API.
old-location: snmp\snmputiloctetsfree.htm
tech.root: SNMP
ms.assetid: be101ab3-393c-4b1a-882d-0284715d1da4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpUtilOctetsFree, SnmpUtilOctetsFree function [SNMP], _snmp_snmputiloctetsfree, snmp.snmputiloctetsfree, snmp/SnmpUtilOctetsFree
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
 - SnmpUtilOctetsFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilOctetsFree function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOctetsFree</b> function frees the memory allocated for the specified octet string. This function is an element of the SNMP Utility API.


## -parameters




### -param pOctets [in]

Pointer to an 
<a href="https://msdn.microsoft.com/d58c54e2-0479-408f-977d-63409e5f500e">AsnOctetString</a> structure whose memory should be freed.


## -returns



This function does not return a value.




## -remarks



Call the 
<b>SnmpUtilOctetsFree</b> function to free the memory that the 
<a href="https://msdn.microsoft.com/5ea92551-f6af-431d-8bf8-5b6c576f3392">SnmpUtilOctetsCpy</a> function allocates.




## -see-also




<a href="https://msdn.microsoft.com/d58c54e2-0479-408f-977d-63409e5f500e">AsnOctetString</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/5ea92551-f6af-431d-8bf8-5b6c576f3392">SnmpUtilOctetsCpy</a>
 

 

