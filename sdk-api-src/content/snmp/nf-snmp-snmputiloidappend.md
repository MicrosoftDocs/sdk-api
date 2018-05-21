---
UID: NF:snmp.SnmpUtilOidAppend
title: SnmpUtilOidAppend function
author: windows-driver-content
description: The SnmpUtilOidAppend function appends the source object identifier to the destination object identifier. This function is an element of the SNMP Utility API.
old-location: snmp\snmputiloidappend.htm
old-project: SNMP
ms.assetid: 8ffa5638-13ef-4cec-80f0-303611a52dac
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SnmpUtilOidAppend, SnmpUtilOidAppend function [SNMP], _snmp_snmputiloidappend, snmp.snmputiloidappend, snmp/SnmpUtilOidAppend
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
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Snmpapi.dll
api_name:
-	SnmpUtilOidAppend
product: Windows
targetos: Windows
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpUtilOidAppend function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidAppend</b> function appends the source object identifier to the destination object identifier. This function is an element of the SNMP Utility API.


## -parameters




### -param pOidDst [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to receive the source structure.


### -param pOidSrc [in]

Pointer to an 
<b>AsnObjectIdentifier</b> structure to append.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. This function does not generate Windows Sockets errors. The application should call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. <b>GetLastError</b> may return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_BERAPI_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Indicates an overflow condition

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MEM_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Indicates a memory allocation error

</td>
</tr>
</table>
 




## -remarks



The 
<b>SnmpUtilOidAppend</b> function calls the 
<a href="https://msdn.microsoft.com/269b6f57-cdef-476a-bf38-f35535d15999">SnmpUtilMemReAlloc</a> function. The 
<b>SnmpUtilMemReAlloc</b> function expands the buffer for the destination object identifier.

Call the 
<a href="https://msdn.microsoft.com/8fc44fdf-956a-4102-bcbb-4cd17a73828c">SnmpUtilOidFree</a> function to free memory that the 
<b>SnmpUtilOidAppend</b> function allocates for the destination.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/269b6f57-cdef-476a-bf38-f35535d15999">SnmpUtilMemReAlloc</a>



<a href="https://msdn.microsoft.com/8fc44fdf-956a-4102-bcbb-4cd17a73828c">SnmpUtilOidFree</a>
 

 

