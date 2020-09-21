---
UID: NF:winsnmp.SnmpEncodeMsg
title: SnmpEncodeMsg function (winsnmp.h)
description: The Microsoft WinSNMP implementation uses the parameters passed in the WinSNMP SnmpEncodeMsg function to encode an SNMP message.
helpviewer_keywords: ["SnmpEncodeMsg","SnmpEncodeMsg function [SNMP]","_snmp_snmpencodemsg","snmp.snmpencodemsg","winsnmp/SnmpEncodeMsg"]
old-location: snmp\snmpencodemsg.htm
tech.root: SNMP
ms.assetid: 0c8ebf49-b59e-4483-a7cf-456794e24bd6
ms.date: 12/05/2018
ms.keywords: SnmpEncodeMsg, SnmpEncodeMsg function [SNMP], _snmp_snmpencodemsg, snmp.snmpencodemsg, winsnmp/SnmpEncodeMsg
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
 - SnmpEncodeMsg
 - winsnmp/SnmpEncodeMsg
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
 - SnmpEncodeMsg
---

# SnmpEncodeMsg function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft WinSNMP implementation uses the parameters passed in the WinSNMP 
<b>SnmpEncodeMsg</b> function to encode an SNMP message. The implementation returns the encoded SNMP message to the WinSNMP application in the buffer specified by the <i>msgBufDesc</i> parameter.

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param srcEntity [in]

Handle to the management entity that initiates the request to encode the SNMP message.

### -param dstEntity [in]

Handle to the target management entity.

### -param context [in]

Handle to the context (a set of managed object resources) that the target management entity controls.

### -param pdu [in]

Handle to the PDU that contains the SNMP operation request.

### -param msgBufDesc [out]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure that receives the encoded SNMP message.

## -returns

If the function succeeds, the return value is the length, in bytes, of the encoded SNMP message. This number is also the value of the <b>len</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure pointed to by the <i>msgBufDesc</i> parameter.

If the function fails, the return value is SNMPAPI_FAILURE. For additional information, see the following Remarks section. To get extended error information, call 
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
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
One or both of the entity parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_CONTEXT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>context</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdu</i> parameter is invalid.

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

The first five parameters passed to the 
<b>SnmpEncodeMsg</b> function are the same parameters that are passed to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function.

The WinSNMP application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to free resources allocated for the <b>ptr</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure. This is the structure pointed to by the <i>msgBufDesc</i> parameter. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

On input, the 
<b>SnmpEncodeMsg</b> function ignores the members of the structure pointed to by the <i>msgBufDesc</i> parameter. The implementation overwrites the members of the structure if the function completes successfully.

The implementation verifies the format of the first five input parameters. If one of the parameters is invalid, 
<b>SnmpEncodeMsg</b> returns SNMPAPI_FAILURE, and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> returns an extended error code.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpdecodemsg">SnmpDecodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a>