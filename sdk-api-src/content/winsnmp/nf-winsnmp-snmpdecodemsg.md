---
UID: NF:winsnmp.SnmpDecodeMsg
title: SnmpDecodeMsg function (winsnmp.h)
description: The WinSNMP SnmpDecodeMsg function decodes an encoded SNMP message into its components. This function performs the opposite action of the WinSNMP SnmpEncodeMsg function.
helpviewer_keywords: ["SnmpDecodeMsg","SnmpDecodeMsg function [SNMP]","_snmp_snmpdecodemsg","snmp.snmpdecodemsg","winsnmp/SnmpDecodeMsg"]
old-location: snmp\snmpdecodemsg.htm
tech.root: SNMP
ms.assetid: d19d6451-1640-4c3b-9e60-d9cb591cf173
ms.date: 12/05/2018
ms.keywords: SnmpDecodeMsg, SnmpDecodeMsg function [SNMP], _snmp_snmpdecodemsg, snmp.snmpdecodemsg, winsnmp/SnmpDecodeMsg
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
 - SnmpDecodeMsg
 - winsnmp/SnmpDecodeMsg
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
 - SnmpDecodeMsg
---

# SnmpDecodeMsg function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpDecodeMsg</b> function decodes an encoded SNMP message into its components. This function performs the opposite action of the WinSNMP 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a> function.

## -parameters

### -param session [in]

Handle to the WinSNMP session. This parameter is required. For additional information, see the following Remarks section.

### -param srcEntity [out]

Pointer to a variable that receives a handle to the source management entity. For more information, see the following Remarks section.

### -param dstEntity [out]

Pointer to a variable that receives a handle to the target management entity. For more information, see the following Remarks section.

### -param context [out]

Pointer to a variable that receives a handle to the context (a set of managed object resources) that the target management entity controls.

### -param pdu [out]

Pointer to a variable that receives a handle to the SNMP protocol data unit (PDU).

### -param msgBufDesc [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure that contains the SNMP message to decode into its components. The <b>len</b> member of the structure specifies the maximum number of bytes to process; the <b>ptr</b> member points to the encoded SNMP message.

## -returns

If the function succeeds, the return value is the number of decoded bytes. This value can be equal to, or less than, the <b>len</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure pointed to by the <i>msgBufDesc</i> parameter.

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
<dt><b>SNMPAPI_OUTPUT_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The output buffer length is insufficient. No output parameters were created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_MESSAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The SNMP message format in the buffer indicated by the <i>msgBufDesc</i> parameter is invalid. No output parameters were created.

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

The Microsoft WinSNMP implementation returns a value of zero in the <i>srcEntity</i> and the <i>dstEntity</i> parameters when an application submits an SNMPv1 or an SNMPv2C message to the 
<b>SnmpDecodeMsg</b> function. This is because the message format does not include the address information necessary to create WinSNMP entity resources.

The Microsoft WinSNMP implementation allocates resources to the WinSNMP application as a result of a successful call to the 
<b>SnmpDecodeMsg</b> function. It is recommended that the WinSNMP application free individual resources with the WinSNMP function that corresponds to the resource. For additional information, see 
<a href="/windows/desktop/SNMP/freeing-winsnmp-descriptors">Freeing WinSNMP Descriptors</a> and 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpencodemsg">SnmpEncodeMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a>