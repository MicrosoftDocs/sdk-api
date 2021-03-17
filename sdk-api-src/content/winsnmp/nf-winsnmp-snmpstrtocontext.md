---
UID: NF:winsnmp.SnmpStrToContext
title: SnmpStrToContext function (winsnmp.h)
description: The WinSNMP SnmpStrToContext function returns a handle to SNMP context information that is specific to the Microsoft WinSNMP implementation.
helpviewer_keywords: ["SNMPAPI_TRANSLATED","SNMPAPI_UNTRANSLATED_V1","SNMPAPI_UNTRANSLATED_V2","SnmpStrToContext","SnmpStrToContext function [SNMP]","_snmp_snmpstrtocontext","snmp.snmpstrtocontext","winsnmp/SnmpStrToContext"]
old-location: snmp\snmpstrtocontext.htm
tech.root: SNMP
ms.assetid: d552f453-cc19-4166-aca3-bbaa3669b1c8
ms.date: 12/05/2018
ms.keywords: SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpStrToContext, SnmpStrToContext function [SNMP], _snmp_snmpstrtocontext, snmp.snmpstrtocontext, winsnmp/SnmpStrToContext
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
 - SnmpStrToContext
 - winsnmp/SnmpStrToContext
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
 - SnmpStrToContext
---

# SnmpStrToContext function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpStrToContext</b> function returns a handle to SNMP context information that is specific to the Microsoft WinSNMP implementation. The handle is a valid value that a WinSNMP application can use as the <i>context</i> parameter in a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a> functions.

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param string [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure that contains a string to interpret. The string can identify a collection of managed objects, or it can be a community string. 




The current setting of the entity and context translation mode determines the way 
<b>SnmpStrToContext</b> interprets the input string structure as shown in the following table.

<table>
<tr>
<th>Entity/Context Translation Mode</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_TRANSLATED"></a><a id="snmpapi_translated"></a><dl>
<dt><b>SNMPAPI_TRANSLATED</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a user-friendly name for a collection of managed objects. The implementation translates the name into its SNMPv1 or SNMPv2C components using the implementation's database.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V1"></a><a id="snmpapi_untranslated_v1"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V1</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP community string.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V2"></a><a id="snmpapi_untranslated_v2"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V2</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP community string.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a handle to the context of interest.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a>. The 
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
<dt><b>SNMPAPI_SESSION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>session</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_CONTEXT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>string</i> parameter format is invalid. For example, the <b>len</b> member or the <b>ptr</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure pointed to by the <i>string</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_CONTEXT_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The value referenced in the <i>string</i> parameter does not exist.

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

The current setting of the entity and context translation mode determines the manner in which 
<b>SnmpStrToContext</b> interprets the input string structure. For additional information, see 
<a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a>.

The WinSNMP application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a> function to release the context handle allocated by the 
<b>SnmpStrToContext</b> function. For additional information about releasing resources, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

The WinSNMP application should free the memory associated with the <b>ptr</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure pointed to by the <i>string</i> parameter. This is because the application defines and allocates the resources. For example, if the application allocated resources with a call to the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function, it should use the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function to deallocate the resources. For additional information, see 
<a href="/windows/desktop/SNMP/freeing-winsnmp-descriptors">Freeing WinSNMP Descriptors</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a>