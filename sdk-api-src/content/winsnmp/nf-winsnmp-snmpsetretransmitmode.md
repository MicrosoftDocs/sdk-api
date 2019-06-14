---
UID: NF:winsnmp.SnmpSetRetransmitMode
title: SnmpSetRetransmitMode function (winsnmp.h)
author: windows-sdk-content
description: The WinSNMP SnmpSetRetransmitMode function enables a WinSNMP application to set the retransmission mode.
old-location: snmp\snmpsetretransmitmode.htm
tech.root: SNMP
ms.assetid: d206ba15-a068-4579-bd6a-ab2444a723e0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SnmpSetRetransmitMode, SnmpSetRetransmitMode function [SNMP], _snmp_snmpsetretransmitmode, snmp.snmpsetretransmitmode, winsnmp/SnmpSetRetransmitMode
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
 - SnmpSetRetransmitMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SnmpSetRetransmitMode function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetRetransmitMode</b> function enables a WinSNMP application to set the retransmission mode. The Microsoft WinSNMP implementation uses the new retransmission mode to govern transmission time-outs and retransmission attempts on subsequent calls to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function.


## -parameters




### -param nRetransmitMode [in]

Specifies a value for the new retransmission mode. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_ON"></a><a id="snmpapi_on"></a><dl>
<dt><b>SNMPAPI_ON</b></dt>
</dl>
</td>
<td width="60%">
The implementation executes the WinSNMP application's retransmission policy.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
The implementation does not execute the WinSNMP application's retransmission policy.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
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
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

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
<dt><b>SNMPAPI_MODE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The implementation does not support the requested retransmission mode.

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



Typically a WinSNMP manager application, rather than an agent application, calls the 
<b>SnmpSetRetransmitMode</b> function.

If a WinSNMP application sets the retransmission mode to SNMPAPI_OFF, the implementation does not initiate retransmission attempts for new SNMP communications operations. The new setting affects all subsequent calls to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function, until the WinSNMP application sets the retransmission mode back to SNMPAPI_ON.

Calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpcancelmsg">SnmpCancelMsg</a> function is equivalent to calling the 
<b>SnmpSetRetransmitMode</b> function, for a specific SNMP message, with the retransmission mode equal to SNMPAPI_OFF.

<div class="alert"><b>Note</b>  If the implementation returns the error SNMPAPI_MODE_INVALID to a call to 
<b>SnmpSetRetransmitMode</b>, the WinSNMP application must execute the retransmission policy.</div>
<div> </div>
For additional information, see 
<a href="https://docs.microsoft.com/windows/desktop/SNMP/about-retransmission">About Retransmission</a> and 
<a href="https://docs.microsoft.com/windows/desktop/SNMP/managing-the-retransmission-policy">Managing the Retransmission Policy</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpcancelmsg">SnmpCancelMsg</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetretransmitmode">SnmpGetRetransmitMode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetretry">SnmpGetRetry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpgettimeout">SnmpGetTimeout</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>
 

 

