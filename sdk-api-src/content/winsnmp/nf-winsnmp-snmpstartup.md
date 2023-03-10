---
UID: NF:winsnmp.SnmpStartup
title: SnmpStartup function (winsnmp.h)
description: The SnmpStartup function notifies the Microsoft WinSNMP implementation that the WinSNMP application requires the implementation's services.
helpviewer_keywords: ["SNMPAPI_OFF","SNMPAPI_ON","SNMPAPI_TRANSLATED","SNMPAPI_UNTRANSLATED_V1","SNMPAPI_UNTRANSLATED_V2","SnmpStartup","SnmpStartup function [SNMP]","_snmp_snmpstartup","snmp.snmpstartup","winsnmp/SnmpStartup"]
old-location: snmp\snmpstartup.htm
tech.root: SNMP
ms.assetid: 7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce
ms.date: 12/05/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpStartup, SnmpStartup function [SNMP], _snmp_snmpstartup, snmp.snmpstartup, winsnmp/SnmpStartup
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
 - SnmpStartup
 - winsnmp/SnmpStartup
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
 - SnmpStartup
---

# SnmpStartup function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpStartup</b> function notifies the Microsoft WinSNMP implementation that the WinSNMP application requires the implementation's services. The WinSNMP 
<b>SnmpStartup</b> function enables the implementation to initialize and to return to the application the version of the Windows SNMP Application Programming Interface (WinSNMP API), the level of SNMP communications that the implementation supports, and the implementation's default translation and retransmission modes.
<div class="alert"><b>Note</b>  A WinSNMP application must call the 
<b>SnmpStartup</b> function successfully before it calls any other WinSNMP function.</div><div> </div>

## -parameters

### -param nMajorVersion [out]

Pointer to an unsigned long integer variable to receive the major version number of the WinSNMP API that the implementation supports. For example, to indicate that the implementation supports WinSNMP version 2.0, the function returns a value of 2.

### -param nMinorVersion [out]

Pointer to an unsigned long integer variable to receive the minor version number of the WinSNMP API that the implementation supports. For example, to indicate that the implementation supports WinSNMP version 2.0, the function returns a value of 0.

### -param nLevel [out]

Pointer to an unsigned long integer variable to receive the highest level of SNMP communications the implementation supports. Upon successful return, this parameter contains a value of 2. For a description of level 2 support, see 
<a href="/windows/desktop/SNMP/levels-of-snmp-support">Levels of SNMP Support</a>.

### -param nTranslateMode [out]

Pointer to an unsigned long integer variable to receive the default translation mode in effect for the implementation. The translation mode applies to the implementation's interpretation of the <i>entity</i> parameter that the WinSNMP application passes to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a> function. The translation mode also applies to the <i>string</i> parameter that the WinSNMP application passes to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtocontext">SnmpStrToContext</a> function. This parameter can be one of the following values. 



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
 

For additional information, see 
<a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a>.

### -param nRetransmitMode [out]

Pointer to an unsigned long integer variable to receive the default retransmission mode in effect for the implementation. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
The implementation is not executing the retransmission policy of the WinSNMP application.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_ON"></a><a id="snmpapi_on"></a><dl>
<dt><b>SNMPAPI_ON</b></dt>
</dl>
</td>
<td width="60%">
The implementation is executing the retransmission policy of the WinSNMP application.

</td>
</tr>
</table>
 

For additional information, see 
<a href="/windows/desktop/SNMP/about-retransmission">About Retransmission</a>.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS, and the parameters contain appropriate values, as indicated in the preceding parameter descriptions.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
<b>SnmpGetLastError</b> function can return one of the following errors. For additional information, see the Remarks section that follows.

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
<b>SnmpStartup</b> function did not complete successfully.

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

A WinSNMP application must call the 
<b>SnmpStartup</b> function successfully at least once, before it calls any other WinSNMP function. If a WinSNMP application does call another WinSNMP function, before it successfully calls 
<b>SnmpStartup</b>, the implementation returns the error SNMPAPI_NOT_INITIALIZED.

The WinSNMP application can call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> for error information, or retry 
<b>SnmpStartup</b> if a call to the 
<b>SnmpStartup</b> function fails. When 
<b>SnmpStartup</b> returns SNMPAPI_FAILURE, and a subsequent call to 
<b>SnmpGetLastError</b> returns SNMP_ALLOC_ERROR, the WinSNMP application can elect to wait. It can retry the call to 
<b>SnmpStartup</b> when the implementation has adequate free resources.

A WinSNMP application can call 
<b>SnmpStartup</b> multiple times. For example, it may need to retry the function call for the reasons discussed preceding. A WinSNMP application must also call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> at least once, as the last WinSNMP function call before it terminates. Multiple 
<b>SnmpStartup</b> calls do not require multiple 
<b>SnmpCleanup</b> calls.

For additional information, see 
<a href="/windows/desktop/SNMP/levels-of-snmp-support">Levels of SNMP Support</a> and 
<a href="/windows/desktop/SNMP/about-snmp-versions">About SNMP Versions</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtocontext">SnmpStrToContext</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>