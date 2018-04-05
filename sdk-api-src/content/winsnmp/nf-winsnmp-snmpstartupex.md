---
UID: NF:winsnmp.SnmpStartupEx
title: SnmpStartupEx function
author: windows-driver-content
description: The SnmpStartupEx function notifies the Microsoft WinSNMP implementation that the WinSNMP application requires the implementation's services.
old-location: snmp\snmpstartupex.htm
old-project: SNMP
ms.assetid: 5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpStartupEx, SnmpStartupEx function [SNMP], _snmp_snmpstartupex, snmp.snmpstartupex, winsnmp/SnmpStartupEx
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
req.typenames: SCARD_IO_REQUEST, *PSCARD_IO_REQUEST, *LPSCARD_IO_REQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsnmp32.dll
api_name:
-	SnmpStartupEx
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpStartupEx function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements 
    section. It may be altered or unavailable in subsequent versions. Instead, use 
    <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft 
    implementation of WS-Man.]

The <b>SnmpStartupEx</b> function notifies the Microsoft 
    WinSNMP implementation that the WinSNMP application requires the implementation's services. The WinSNMP 
    <b>SnmpStartupEx</b> function enables the implementation to 
    initialize and to return to the application the version of the Windows SNMP Application Programming Interface (WinSNMP API), the level of SNMP communications that the implementation supports, and the implementation's default translation and retransmission modes.

This function should be used instead of <a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> if Windows Server 2003 with Service Pack 1 (SP1) or later is installed. <b>SnmpStartupEx</b> enables support for multiple independent software modules that use WinSNMP within the same application.
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
      <a href="https://msdn.microsoft.com/9874ad9b-4eb9-4d63-816b-fe444c5b4d8a">Levels of SNMP Support</a>.


### -param nTranslateMode [out]

Pointer to an unsigned long integer variable to receive the default translation mode in effect for 
      the implementation. The translation mode applies to how the implementation interprets the 
      <i>entity</i> parameter, that the WinSNMP application passes to the 
      <a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a> function. The translation mode also 
      applies to the <i>string</i> parameter that the WinSNMP application passes to the 
      <a href="https://msdn.microsoft.com/d552f453-cc19-4166-aca3-bbaa3669b1c8">SnmpStrToContext</a> function. This parameter can be 
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
       <a href="https://msdn.microsoft.com/2550f235-1351-440a-8b4e-f0d30b058229">Setting the Entity and Context Translation Mode</a>.


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
       <a href="https://msdn.microsoft.com/71150a66-74a3-4957-bc70-3dd25c3b9c71">About Retransmission</a>.


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS, and the parameters contain appropriate values, 
       as indicated in the preceding parameter descriptions.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
       <a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a> specifying a 
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
The <a href="https://msdn.microsoft.com/5f0c9da1-d18e-4f93-8b5c-c5ad18360a7a">SnmpStartupEx</a> function did not initialize correctly.

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
   <a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a> for error information, or 
   retry <b>SnmpStartupEx</b> if a call to the 
   <b>SnmpStartupEx</b> function fails. When 
   <b>SnmpStartupEx</b> returns SNMPAPI_FAILURE, and a subsequent 
   call to <b>SnmpGetLastError</b> returns SNMP_ALLOC_ERROR, the 
   WinSNMP application can elect to wait. It can retry the call to 
   <b>SnmpStartupEx</b> when the implementation has adequate free 
   resources.

A WinSNMP application must call <a href="https://msdn.microsoft.com/e6521c35-a58e-4b8e-b415-b49954187736">SnmpCleanupEx</a> for 
   each successful call to <b>SnmpStartupEx</b>. The WinSNMP 
   implementation performs the final cleanup where there are no outstanding successful calls to <a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> or <b>SnmpStartupEx</b>.

For additional information, see 
   <a href="https://msdn.microsoft.com/9874ad9b-4eb9-4d63-816b-fe444c5b4d8a">Levels of SNMP Support</a> and 
   <a href="https://msdn.microsoft.com/7de41e08-3cb3-454a-aa4e-140a35c99472">About SNMP Versions</a>.




## -see-also




<a href="https://msdn.microsoft.com/e6521c35-a58e-4b8e-b415-b49954187736">SnmpCleanupEx</a>



<a href="https://msdn.microsoft.com/d552f453-cc19-4166-aca3-bbaa3669b1c8">SnmpStrToContext</a>



<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP Functions</a>
 

 

