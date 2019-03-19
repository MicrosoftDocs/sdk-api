---
UID: NF:snmp.SnmpUtilOctetsCpy
title: SnmpUtilOctetsCpy function (snmp.h)
author: windows-sdk-content
description: The SnmpUtilOctetsCpy function copies the variable pointed to by the pOctetsSrc parameter to the variable pointed to by the pOctetsDst parameter.
old-location: snmp\snmputiloctetscpy.htm
tech.root: SNMP
ms.assetid: 5ea92551-f6af-431d-8bf8-5b6c576f3392
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpUtilOctetsCpy, SnmpUtilOctetsCpy function [SNMP], _snmp_snmputiloctetscpy, snmp.snmputiloctetscpy, snmp/SnmpUtilOctetsCpy
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
 - SnmpUtilOctetsCpy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpUtilOctetsCpy function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOctetsCpy</b> function copies the variable pointed to by the <i>pOctetsSrc</i> parameter to the variable pointed to by the <i>pOctetsDst</i> parameter. The function allocates any necessary memory for the destination's copy. The 
<b>SnmpUtilOctetsCpy</b> function is an element of the SNMP Utility API.


## -parameters




### -param pOctetsDst [out]

Pointer to an 
<a href="https://msdn.microsoft.com/d58c54e2-0479-408f-977d-63409e5f500e">AsnOctetString</a> structure to receive the copy.


### -param pOctetsSrc [in]

Pointer to an 
<b>AsnOctetString</b> structure to copy.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/be101ab3-393c-4b1a-882d-0284715d1da4">SnmpUtilOctetsFree</a> function to free the memory that the 
<b>SnmpUtilOctetsCpy</b> function allocates for the destination structure.




## -see-also




<a href="https://msdn.microsoft.com/d58c54e2-0479-408f-977d-63409e5f500e">AsnOctetString</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/be101ab3-393c-4b1a-882d-0284715d1da4">SnmpUtilOctetsFree</a>
 

 

