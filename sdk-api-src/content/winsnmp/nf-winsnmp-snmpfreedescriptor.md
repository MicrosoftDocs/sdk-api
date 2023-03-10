---
UID: NF:winsnmp.SnmpFreeDescriptor
title: SnmpFreeDescriptor function (winsnmp.h)
description: A WinSNMP application uses the SnmpFreeDescriptor function to inform the Microsoft WinSNMP implementation that it no longer requires access to a descriptor object.
helpviewer_keywords: ["SnmpFreeDescriptor","SnmpFreeDescriptor function [SNMP]","_snmp_snmpfreedescriptor","snmp.snmpfreedescriptor","winsnmp/SnmpFreeDescriptor"]
old-location: snmp\snmpfreedescriptor.htm
tech.root: SNMP
ms.assetid: 535f728d-6964-47b6-9913-7cd38356053d
ms.date: 12/05/2018
ms.keywords: SnmpFreeDescriptor, SnmpFreeDescriptor function [SNMP], _snmp_snmpfreedescriptor, snmp.snmpfreedescriptor, winsnmp/SnmpFreeDescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpFreeDescriptor
 - winsnmp/SnmpFreeDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpFreeDescriptor
---

# SnmpFreeDescriptor function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application uses the 
<b>SnmpFreeDescriptor</b> function to inform the Microsoft WinSNMP implementation that it no longer requires access to a descriptor object. This WinSNMP function signals the implementation to free the memory it allocated for the descriptor object.

## -parameters

### -param syntax [in]

Specifies the syntax data type of the target descriptor object.

### -param descriptor [in]

Pointer to an <b>smiOPAQUE</b> structure that contains the target descriptor object to release.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
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
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

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
<dt><b>SNMPAPI_SYNTAX_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>syntax</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OPERATION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>descriptor</i> parameter is invalid. For additional information, see the following Remarks section.

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

The implementation allocates and deallocates memory for output descriptor objects with variable lengths. This memory allocation and deallocation are restricted to the implementation, except for the interface that the 
<b>SnmpFreeDescriptor</b> function provides. For additional information, see 
<a href="/windows/desktop/SNMP/freeing-winsnmp-descriptors">Freeing WinSNMP Descriptors</a>.

The implementation returns the SNMPAPI_OPERATION_INVALID error code if the <i>descriptor</i> parameter specifies a memory allocation that the implementation released in a prior call to 
<b>SnmpFreeDescriptor</b>. The function returns the same error code if the <i>descriptor</i> parameter specifies a memory allocation that the implementation did not make for the calling WinSNMP application.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpoidcopy">SnmpOidCopy</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtooid">SnmpStrToOid</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>