---
UID: NF:lmwksta.NetWkstaTransportAdd
title: NetWkstaTransportAdd function (lmwksta.h)
description: Not supported. (NetWkstaTransportAdd)
helpviewer_keywords: ["0","NetWkstaTransportAdd","NetWkstaTransportAdd function [Network Management]","_win32_netwkstatransportadd","lmwksta/NetWkstaTransportAdd","netmgmt.netwkstatransportadd"]
old-location: netmgmt\netwkstatransportadd.htm
tech.root: NetMgmt
ms.assetid: 016060ea-eae1-421f-b708-5c2ddd2000c1
ms.date: 12/05/2018
ms.keywords: 0, NetWkstaTransportAdd, NetWkstaTransportAdd function [Network Management], _win32_netwkstatransportadd, lmwksta/NetWkstaTransportAdd, netmgmt.netwkstatransportadd
req.header: lmwksta.h
req.include-header: Lm.h, Lmwksta.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetWkstaTransportAdd
 - lmwksta/NetWkstaTransportAdd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetWkstaTransportAdd
---

# NetWkstaTransportAdd function


## -description

<p class="CCE_Message">[This function is obsolete. To change the default settings for transport protocols manually, use the <b>Local Area Connection Properties</b> dialog box in the <b>Network and Dial-Up Connections</b> folder.]

Not supported.

The 
				<b>NetWkstaTransportAdd</b> function binds (or connects) the redirector to the transport. The redirector is the software on the client computer which generates file requests to the server computer.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 


This string must begin with \\.

### -param level [in]

Specifies the information level of the data. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Specifies workstation transport protocol information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_transport_info_0">WKSTA_TRANSPORT_INFO_0</a> structure.

</td>
</tr>
</table>

### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first parameter that causes the ERROR_INVALID_PARAMETER error. If this parameter is <b>NULL</b>, the index is not returned on error.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The level parameter, which indicates what level of data structure information is available, is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators local group can successfully execute the 
<b>NetWkstaTransportAdd</b> function.

If the 
<b>NetWkstaTransportAdd</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>parm_err</i> parameter to indicate the member of the 
<b>WKSTA_TRANSPORT_INFO_0</b> structure that is invalid. The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error.

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>TRANSPORT_QUALITYOFSERVICE_PARMNUM</td>
<td><b>wkti0_quality_of_service</b></td>
</tr>
<tr>
<td>TRANSPORT_NAME_PARMNUM</td>
<td><b>wkti0_transport_name</b></td>
</tr>
</table>
