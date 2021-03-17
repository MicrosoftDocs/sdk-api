---
UID: NS:lmuse._USE_INFO_3
title: USE_INFO_3 (lmuse.h)
description: The USE_INFO_3 structure contains information about a connection between a local computer and a shared resource, including connection type, connection status, user name, domain name, and specific flags that describe connection behavior.
helpviewer_keywords: ["*LPUSE_INFO_3","*PUSE_INFO_3","CREATE_BYPASS_CSC","CREATE_NO_CONNECT","LPUSE_INFO_0","LPUSE_INFO_0 structure pointer [Network Management]","PUSE_INFO_3","PUSE_INFO_3 structure pointer [Network Management]","USE_DEFAULT_CREDENTIALS","USE_INFO_3","USE_INFO_3 structure [Network Management]","lmuse/LPUSE_INFO_0","lmuse/PUSE_INFO_3","lmuse/USE_INFO_3","netmgmt.use_info_3_str"]
old-location: netmgmt\use_info_3_str.htm
tech.root: NetMgmt
ms.assetid: 3fb3ad35-f9e5-46ba-b930-fc2ccafd8ee9
ms.date: 12/05/2018
ms.keywords: '*LPUSE_INFO_3, *PUSE_INFO_3, CREATE_BYPASS_CSC, CREATE_NO_CONNECT, LPUSE_INFO_0, LPUSE_INFO_0 structure pointer [Network Management], PUSE_INFO_3, PUSE_INFO_3 structure pointer [Network Management], USE_DEFAULT_CREDENTIALS, USE_INFO_3, USE_INFO_3 structure [Network Management], lmuse/LPUSE_INFO_0, lmuse/PUSE_INFO_3, lmuse/USE_INFO_3, netmgmt.use_info_3_str'
req.header: lmuse.h
req.include-header: Lm.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: USE_INFO_3, *PUSE_INFO_3, *LPUSE_INFO_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USE_INFO_3
 - lmuse/_USE_INFO_3
 - PUSE_INFO_3
 - lmuse/PUSE_INFO_3
 - USE_INFO_3
 - lmuse/USE_INFO_3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmuse.h
api_name:
 - USE_INFO_3
---

## -description

The <b>USE_INFO_3</b> structure contains information about a connection between a local computer and a shared resource, including connection type, connection status, user name, domain name, and specific flags that describe connection behavior.

## -struct-fields

### -field ui3_ui2

<a href="/windows/desktop/api/lmuse/ns-lmuse-use_info_2">USE_INFO_2</a> structure that contains

### -field ui3_flags

A set of bit flags that describe connection behavior and credential handling.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_NO_CONNECT"></a><a id="create_no_connect"></a><dl>
<dt><b>CREATE_NO_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
Do not connect to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_BYPASS_CSC"></a><a id="create_bypass_csc"></a><dl>
<dt><b>CREATE_BYPASS_CSC</b></dt>
</dl>
</td>
<td width="60%">
Force a connection to the server, bypassing the CSC.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_DEFAULT_CREDENTIALS"></a><a id="use_default_credentials"></a><dl>
<dt><b>USE_DEFAULT_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
No explicit credentials are supplied in the call to <a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseenum">NetUseEnum</a>



<a href="/windows/desktop/api/lmuse/nf-lmuse-netusegetinfo">NetUseGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/use-functions">Use functions</a>
