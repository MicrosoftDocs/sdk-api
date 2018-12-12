---
UID: NF:winsnmp.SnmpSetVb
title: SnmpSetVb function
author: windows-sdk-content
description: The WinSNMP SnmpSetVb function changes variable binding entries in a variable bindings list. This function also appends new variable binding entries to an existing variable bindings list.
old-location: snmp\snmpsetvb.htm
tech.root: SNMP
ms.assetid: 65d962bd-f4d7-4cf4-9b24-a7678e669e24
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpSetVb, SnmpSetVb function [SNMP], _snmp_snmpsetvb, snmp.snmpsetvb, winsnmp/SnmpSetVb
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpSetVb
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpSetVb function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetVb</b> function changes variable binding entries in a variable bindings list. This function also appends new variable binding entries to an existing variable bindings list.


## -parameters




### -param vbl [in]

Handle to the variable bindings list to update.


### -param index [in]

Specifies an unsigned long integer variable that contains the position of the variable binding entry, within the variable bindings list, if this is an update operation. If this is an append operation, this parameter must be equal to zero. For more information, see the following Remarks section.


### -param name [in]

Pointer to an 
<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a> structure that represents the name of the variable to append or change. For more information, see the following Remarks section.


### -param value [in]

Pointer to an 
<a href="https://msdn.microsoft.com/en-us/library/Aa377997(v=VS.85).aspx">smiVALUE</a> structure. The structure contains the value associated with the variable specified by the <i>name</i> parameter.


## -returns



If the function succeeds, the return value is the position of the updated or appended variable binding entry in the variable bindings list. For additional information, see the following Remarks section.

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
<dt><b>SNMPAPI_VBL_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>vbl</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_INDEX_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_SYNTAX_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>syntax</b> member of the structure pointed to by the <i>value</i> parameter is invalid.

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



Valid values for the <i>index</i> parameter range from zero to n. The value zero indicates an append operation. The value n is the total number of variable binding entries in the variable bindings list. A WinSNMP application should call the 
<a href="https://msdn.microsoft.com/08e7d450-0c75-4ef5-a9c5-ef0255601a9a">SnmpCountVbl</a> function before it calls 
<b>SnmpSetVb</b> to obtain the total number of variable binding entries.

If the function successfully performs an update operation, the return value equals the value of the <i>index</i> parameter. If the function appends a variable binding entry, the return value is n + 1.

If the <i>name</i> parameter is not <b>NULL</b>, but the <i>value</i> parameter is <b>NULL</b>, the Microsoft WinSNMP implementation initializes the new variable binding entry with the <b>value</b> member set to <b>NULL</b> and with the <b>syntax</b> member set to <a href="https://msdn.microsoft.com/2d87aeee-6fcb-4837-b091-6a9def8a9acb">SNMP_SYNTAX_</a>.

If the <i>index</i> parameter is not equal to zero, and the <i>name</i> parameter is <b>NULL</b>, the Microsoft WinSNMP implementation updates only the value of the variable pointed to by the <i>index</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/08e7d450-0c75-4ef5-a9c5-ef0255601a9a">SnmpCountVbl</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377997(v=VS.85).aspx">smiVALUE</a>
 

 

