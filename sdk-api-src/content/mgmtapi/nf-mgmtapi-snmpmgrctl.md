---
UID: NF:mgmtapi.SnmpMgrCtl
title: SnmpMgrCtl function (mgmtapi.h)
description: The SnmpMgrCtl function sets an operating parameter associated with an SNMP session. This function is an element of the SNMP Management API.
helpviewer_keywords: ["SnmpMgrCtl","SnmpMgrCtl function [SNMP]","_snmp_snmpmgrctl","mgmtapi/SnmpMgrCtl","snmp.snmpmgrctl"]
old-location: snmp\snmpmgrctl.htm
tech.root: SNMP
ms.assetid: d777c944-a19f-4465-ae56-b60beaa1191c
ms.date: 12/05/2018
ms.keywords: SnmpMgrCtl, SnmpMgrCtl function [SNMP], _snmp_snmpmgrctl, mgmtapi/SnmpMgrCtl, snmp.snmpmgrctl
req.header: mgmtapi.h
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
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpMgrCtl
 - mgmtapi/SnmpMgrCtl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mgmtapi.dll
api_name:
 - SnmpMgrCtl
---

# SnmpMgrCtl function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrCtl</b> function sets an operating parameter associated with an SNMP session. This function is an element of the SNMP Management API.

## -parameters

### -param session [in]

Pointer to an internal structure that specifies the session to which the control code applies.

### -param dwCtlCode [in]

Specifies a value (a control code) that identifies the operation to perform. 




Currently, MGMCTL_SETAGENTPORT is the only supported control code. Setting this code allows an SNMP management application to send requests to a remote agent that is "listening" for SNMP manager requests on an arbitrary port. For more information, see the <i>lpvInBuffer</i> and the <i>cbInBuffer</i> parameter descriptions.

### -param lpvInBuffer [in]

Pointer to the buffer that contains the input parameters required for the operation. 




When you specify the MGMCTL_SETAGENTPORT control code, this parameter must point to an unsigned integer that specifies the port number on which the remote agent will "listen" for SNMP manager requests. The port number must be in host-byte order.

### -param cbInBuffer [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>lpvInBuffer</i> parameter. 




When you specify the MGMCTL_SETAGENTPORT control code, this parameter is equal to sizeof(UINT).

### -param lpvOUTBuffer [out]

Pointer to the buffer that receives the operation's output data.

### -param cbOUTBuffer [out]

Specifies the size, in bytes, of the buffer pointed to by the <i>lpvOutBuffer</i> parameter.

### -param lpcbBytesReturned [out]

Pointer to a variable that receives the actual size, in bytes, of the data stored in the buffer pointed to by the <i>lpvOutBuffer</i> parameter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> can also return one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_INVALID_CTL</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwCtlCode</i> parameter does not specify a valid control code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_INVALID_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The <i>session</i> parameter does not specify a valid SNMP session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_INVALID_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the <i>lpvInBuffer</i>, <i>lpvOutBuffer</i>, or <i>lpcbBytesRequired</i> parameters are invalid, or the <i>cbInBuffer</i> or <i>cbOutBuffer</i> parameter is too small.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgropen">SnmpMgrOpen</a>