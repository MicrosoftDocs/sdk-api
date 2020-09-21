---
UID: NF:winsnmp.SnmpStrToEntity
title: SnmpStrToEntity function (winsnmp.h)
description: The WinSNMP SnmpStrToEntity function returns a handle to information about an SNMP management entity that is specific to the Microsoft WinSNMP implementation.
helpviewer_keywords: ["SNMPAPI_TRANSLATED","SNMPAPI_UNTRANSLATED_V1","SNMPAPI_UNTRANSLATED_V2","SnmpStrToEntity","SnmpStrToEntity function [SNMP]","_snmp_snmpstrtoentity","snmp.snmpstrtoentity","winsnmp/SnmpStrToEntity"]
old-location: snmp\snmpstrtoentity.htm
tech.root: SNMP
ms.assetid: d0a8e389-ba5b-45f4-9682-1fbe456daaed
ms.date: 12/05/2018
ms.keywords: SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpStrToEntity, SnmpStrToEntity function [SNMP], _snmp_snmpstrtoentity, snmp.snmpstrtoentity, winsnmp/SnmpStrToEntity
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
 - SnmpStrToEntity
 - winsnmp/SnmpStrToEntity
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
 - SnmpStrToEntity
---

# SnmpStrToEntity function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpStrToEntity</b> function returns a handle to information about an SNMP management entity that is specific to the Microsoft WinSNMP implementation.

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param string [in]

Pointer to a null-terminated string that identifies the SNMP management entity of interest. The current setting of the entity and context translation mode determines the manner in which 
<b>SnmpStrToEntity</b> interprets the input string as follows. 



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
The implementation interprets the <i>string</i> parameter as a user-friendly name. The implementation translates the name into its SNMPv1 or SNMPv2C components using the implementation's database.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V1"></a><a id="snmpapi_untranslated_v1"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V1</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP transport address.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V2"></a><a id="snmpapi_untranslated_v2"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V2</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP transport address.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a handle to the SNMP management entity of interest.

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
<dt><b>SNMPAPI_ENTITY_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The entity string is invalid.

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
<b>SnmpStrToEntity</b> interprets the input string that identifies the management entity of interest. For additional information, see 
<a href="/windows/desktop/SNMP/support-for-ipx-address-strings-in-winsnmp">Support for IPX Address Strings in WinSNMP</a> and 
<a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a>.

The WinSNMP application should call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a> function to release the entity handle allocated by the 
<b>SnmpStrToEntity</b> function. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

The 
<b>SnmpStrToEntity</b> function returns a valid entity handle that a WinSNMP application can use as the <i>srcEntity</i> or the <i>dstEntity</i> parameter in multiple WinSNMP functions. These functions include the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a>, and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpdecodemsg">SnmpDecodeMsg</a> functions.

The implementation returns the current entity and context translation mode in the <i>nTranslateMode</i> parameter of the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function. A WinSNMP application can change the setting of the entity and context translation mode with a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsettranslatemode">SnmpSetTranslateMode</a> function.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpdecodemsg">SnmpDecodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsettranslatemode">SnmpSetTranslateMode</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>