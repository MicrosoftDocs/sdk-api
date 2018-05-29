---
UID: NF:winsnmp.SnmpSetPduData
title: SnmpSetPduData function
author: windows-sdk-content
description: The WinSNMP SnmpSetPduData function updates selected data fields in the specified SNMP protocol data unit (PDU).
old-location: snmp\snmpsetpdudata.htm
old-project: SNMP
ms.assetid: 113c67b4-65d7-418d-9600-d1545e1cb0fb
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SnmpSetPduData, SnmpSetPduData function [SNMP], _snmp_snmpsetpdudata, snmp.snmpsetpdudata, winsnmp/SnmpSetPduData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsnmp.h
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsnmp32.dll
api_name:
-	SnmpSetPduData
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpSetPduData function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetPduData</b> function updates selected data fields in the specified SNMP protocol data unit (PDU).


## -parameters




### -param PDU [in]

Handle to an SNMP PDU.


### -param PDU_type [in]

Pointer to a variable with a value to update the <b>PDU_type</b> field of the specified PDU. This parameter can also be <b>NULL</b>.


### -param request_id [in]

Pointer to a variable with a value to update the <b>request_id</b> field of the specified PDU. This parameter can also be <b>NULL</b>.


### -param non_repeaters [in]

If the <i>PDU_type</i> parameter is equal to <a href="https://msdn.microsoft.com/2d87aeee-6fcb-4837-b091-6a9def8a9acb">SNMP_PDU_GETBULK</a>, this parameter points to a variable with a value to update the <b>non_repeaters</b> field of the specified PDU. The Microsoft WinSNMP implementation ignores this parameter for other PDU types. This parameter can also be <b>NULL</b>.


### -param max_repetitions [in]

If the <i>PDU_type</i> parameter is equal to <a href="https://msdn.microsoft.com/2d87aeee-6fcb-4837-b091-6a9def8a9acb">SNMP_PDU_GETBULK</a>, this parameter points to a variable with a value to update the <b>max_repetitions</b> field of the specified PDU. The implementation ignores this parameter for other PDU types. This parameter can also be <b>NULL</b>.


### -param varbindlist [in]

Pointer to a variable with a value that updates the handle to the variable bindings list field of the specified PDU. This parameter can also be <b>NULL</b>.


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a>. The 
<b>SnmpGetLastError</b> function can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> function did not complete successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The PDU type is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_VBL_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The variable bindings list is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
All input parameters are <b>NULL</b>. The SNMP operation was not performed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>
 




## -remarks



All parameters of the 
<b>SnmpSetPduData</b> function are required. However, all parameters, except the <i>PDU</i> parameter, can be <b>NULL</b>. If the WinSNMP application passes <b>NULL</b> in a parameter, 
<b>SnmpSetPduData</b> does not update the corresponding field in the PDU. Because 
<b>SnmpSetPduData</b> passes parameters as pointers to values, an application can still update a PDU field with <b>NULL</b>.

The value of one PDU field can be valid alone, but may be invalidated in combination with values for other fields. The implementation validates the PDU and the other message elements when the application calls the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> or the 
<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a> functions. The implementation rejects invalid PDUs.

The only type of trap PDU you can update with a call to the 
<b>SnmpSetPduData</b> function is an SNMPv2C trap PDU.




## -see-also




<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

