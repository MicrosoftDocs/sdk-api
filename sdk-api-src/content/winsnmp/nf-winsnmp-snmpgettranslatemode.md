---
UID: NF:winsnmp.SnmpGetTranslateMode
title: SnmpGetTranslateMode function (winsnmp.h)
description: The WinSNMP SnmpGetTranslateMode function returns the current setting of the entity and context translation mode to a WinSNMP application.
helpviewer_keywords: ["SNMPAPI_TRANSLATED","SNMPAPI_UNTRANSLATED_V1","SNMPAPI_UNTRANSLATED_V2","SnmpGetTranslateMode","SnmpGetTranslateMode function [SNMP]","_snmp_snmpgettranslatemode","snmp.snmpgettranslatemode","winsnmp/SnmpGetTranslateMode"]
old-location: snmp\snmpgettranslatemode.htm
tech.root: SNMP
ms.assetid: 244bddc1-37fc-4f5b-a1d0-99fd7a76c7a2
ms.date: 12/05/2018
ms.keywords: SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpGetTranslateMode, SnmpGetTranslateMode function [SNMP], _snmp_snmpgettranslatemode, snmp.snmpgettranslatemode, winsnmp/SnmpGetTranslateMode
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
 - SnmpGetTranslateMode
 - winsnmp/SnmpGetTranslateMode
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
 - SnmpGetTranslateMode
---

# SnmpGetTranslateMode function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpGetTranslateMode</b> function returns the current setting of the entity and context translation mode to a WinSNMP application. The entity and context translation mode affects the interpretation and return of WinSNMP input and output string parameters.

## -parameters

### -param nTranslateMode [out]

Pointer to an unsigned long integer variable to receive the entity and context translation mode in effect for the Microsoft WinSNMP implementation. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_TRANSLATED"></a><a id="snmpapi_translated"></a><dl>
<dt><b>SNMPAPI_TRANSLATED</b></dt>
</dl>
</td>
<td width="60%">
The implementation uses its database to translate user-friendly names for SNMP entities and managed objects. The implementation translates them into their SNMPv1 or SNMPv2C components.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V1"></a><a id="snmpapi_untranslated_v1"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V1</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets SNMP entity parameters as SNMP transport addresses, and context parameters as SNMP community strings. For SNMPv2 destination entities, the implementation creates outgoing SNMP messages that contain a value of zero in the version field.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V2"></a><a id="snmpapi_untranslated_v2"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V2</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets SNMP entity parameters as SNMP transport addresses, and context parameters as SNMP community strings. For SNMPv2 destination entities, the implementation creates outgoing SNMP messages that contain a value of 1 in the version field.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. If 
<b>SnmpGetTranslateMode</b> fails, the value of the <i>nTranslateMode</i> parameter has no meaning for the application. To get extended error information, call 
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
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>

## -remarks

The entity and context translation mode affects calls to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtocontext">SnmpStrToContext</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcontexttostr">SnmpContextToStr</a> and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpentitytostr">SnmpEntityToStr</a> functions. For additional information, see 
<a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcontexttostr">SnmpContextToStr</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpentitytostr">SnmpEntityToStr</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsettranslatemode">SnmpSetTranslateMode</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtocontext">SnmpStrToContext</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>