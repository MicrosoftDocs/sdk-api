---
UID: NF:winsnmp.SnmpStartupEx
title: SnmpStartupEx function (winsnmp.h)
description: The SnmpStartupEx function notifies the Microsoft WinSNMP implementation that the WinSNMP application requires the implementation's services.
helpviewer_keywords: ["SNMPAPI_OFF","SNMPAPI_ON","SNMPAPI_TRANSLATED","SNMPAPI_UNTRANSLATED_V1","SNMPAPI_UNTRANSLATED_V2","SnmpStartupEx","SnmpStartupEx function [SNMP]","_snmp_snmpstartupex","snmp.snmpstartupex","winsnmp/SnmpStartupEx"]
old-location: snmp\snmpstartupex.htm
tech.root: SNMP
ms.assetid: 5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a
ms.date: 12/05/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpStartupEx, SnmpStartupEx function [SNMP], _snmp_snmpstartupex, snmp.snmpstartupex, winsnmp/SnmpStartupEx
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
 - SnmpStartupEx
 - winsnmp/SnmpStartupEx
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
 - SnmpStartupEx
---

# SnmpStartupEx function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements 
    section. It may be altered or unavailable in subsequent versions. Instead, use 
    <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft 
    implementation of WS-Man.]

The <b>SnmpStartupEx</b> function notifies the Microsoft 
    WinSNMP implementation that the WinSNMP application requires the implementation's services. The WinSNMP 
    <b>SnmpStartupEx</b> function enables the implementation to 
    initialize and to return to the application the version of the Windows SNMP Application Programming Interface (WinSNMP API), the level of SNMP communications that the implementation supports, and the implementation's default translation and retransmission modes.

This function should be used instead of <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> if Windows Server 2003 with Service Pack 1 (SP1) or later is installed. <b>SnmpStartupEx</b> enables support for multiple independent software modules that use WinSNMP within the same application.
<div class="alert"><b>Note</b>  A WinSNMP application must call the <b>SnmpStartupEx</b> 
    function successfully before it calls any other WinSNMP function.</div><div> </div>

## -parameters

### -param nMajorVersion [out]

Pointer to an unsigned long integer variable to receive the major version number of the WinSNMP API that 
      the implementation supports. For example, to indicate that the implementation supports WinSNMP version 2.0, the 
      function returns a value of 2.

### -param nMinorVersion [out]

Pointer to an unsigned long integer variable to receive the minor version number of the WinSNMP API that 
      the implementation supports. For example, to indicate that the implementation supports WinSNMP version 2.0, the function returns a value of 0.

### -param nLevel [out]

Pointer to an unsigned long integer variable to receive the highest level of SNMP communications the 
      implementation supports. Upon successful return, this parameter contains a value of 2. For a description of level 2 support, see 
      <a href="/windows/desktop/SNMP/levels-of-snmp-support">Levels of SNMP Support</a>.

### -param nTranslateMode [out]

Pointer to an unsigned long integer variable to receive the default translation mode in effect for 
      the implementation. The translation mode applies to how the implementation interprets the 
      <i>entity</i> parameter, that the WinSNMP application passes to the 
      <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a> function. The translation mode also 
      applies to the <i>string</i> parameter that the WinSNMP application passes to the 
      <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtocontext">SnmpStrToContext</a> function. This parameter can be 
      one of the following values.

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
The implementation uses its database to translate user-friendly names for SNMP entities and managed 
        objects. The implementation translates them into their SNMPv1 or SNMPv2C components.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V1"></a><a id="snmpapi_untranslated_v1"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V1</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets SNMP entity parameters as SNMP transport addresses, and context parameters 
        as SNMP community strings. For SNMPv2 destination entities, the implementation creates outgoing SNMP messages 
        that contain a value of zero in the version field.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V2"></a><a id="snmpapi_untranslated_v2"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V2</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets SNMP entity parameters as SNMP transport addresses, and context parameters 
        as SNMP community strings. For SNMPv2 destination entities, the implementation creates outgoing SNMP messages 
        that contain a value of 1 in the version field.

</td>
</tr>
</table>
 

For additional information, see 
       <a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a>.

### -param nRetransmitMode [out]

Pointer to an unsigned long integer variable to receive the default retransmission mode in effect for the 
      implementation. This parameter can be one of the following values.

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

If the function succeeds, the return value is SNMPAPI_SUCCESS, and the parameters contain appropriate values, 
       as indicated in the preceding parameter descriptions.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
       <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a 
       <b>NULL</b> value in its <i>session</i> parameter. The 
       <b>SnmpGetLastError</b> function can return one of the 
       following errors. For additional information, see the "Remarks" section later in this document.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_RESOURCE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A resource allocation error occurred during startup.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartupex">SnmpStartupEx</a> function did not initialize correctly.

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

A WinSNMP application must call the <b>SnmpStartupEx</b> 
   function successfully at least once, before it calls any other WinSNMP function. If a WinSNMP application  calls 
   another WinSNMP function before it successfully calls 
   <b>SnmpStartupEx</b>, the implementation returns the error 
   SNMPAPI_NOT_INITIALIZED.

The WinSNMP application can call 
   <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> for error information, or 
   retry <b>SnmpStartupEx</b> if a call to the 
   <b>SnmpStartupEx</b> function fails. When 
   <b>SnmpStartupEx</b> returns SNMPAPI_FAILURE, and a subsequent 
   call to <b>SnmpGetLastError</b> returns SNMP_ALLOC_ERROR, the 
   WinSNMP application can elect to wait. It can retry the call to 
   <b>SnmpStartupEx</b> when the implementation has adequate free 
   resources.

A WinSNMP application must call <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanupex">SnmpCleanupEx</a> for 
   each successful call to <b>SnmpStartupEx</b>. The WinSNMP 
   implementation performs the final cleanup where there are no outstanding successful calls to <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> or <b>SnmpStartupEx</b>.

For additional information, see 
   <a href="/windows/desktop/SNMP/levels-of-snmp-support">Levels of SNMP Support</a> and 
   <a href="/windows/desktop/SNMP/about-snmp-versions">About SNMP Versions</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanupex">SnmpCleanupEx</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtocontext">SnmpStrToContext</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP Functions</a>