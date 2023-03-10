---
UID: NS:lmaccess._USER_INFO_1010
title: USER_INFO_1010 (lmaccess.h)
description: The USER_INFO_1010 structure contains a set of bit flags defining the operator privileges assigned to a user network account. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1010","*PUSER_INFO_1010","AF_OP_ACCOUNTS","AF_OP_COMM","AF_OP_PRINT","AF_OP_SERVER","LPUSER_INFO_1010","LPUSER_INFO_1010 structure pointer [Network Management]","PUSER_INFO_1010","PUSER_INFO_1010 structure pointer [Network Management]","USER_INFO_1010","USER_INFO_1010 structure [Network Management]","_win32_user_info_1010_str","lmaccess/LPUSER_INFO_1010","lmaccess/PUSER_INFO_1010","lmaccess/USER_INFO_1010","netmgmt.user_info_1010_str"]
old-location: netmgmt\user_info_1010_str.htm
tech.root: NetMgmt
ms.assetid: 6760729a-1d59-430e-8412-1257977af169
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1010, *PUSER_INFO_1010, AF_OP_ACCOUNTS, AF_OP_COMM, AF_OP_PRINT, AF_OP_SERVER, LPUSER_INFO_1010, LPUSER_INFO_1010 structure pointer [Network Management], PUSER_INFO_1010, PUSER_INFO_1010 structure pointer [Network Management], USER_INFO_1010, USER_INFO_1010 structure [Network Management], _win32_user_info_1010_str, lmaccess/LPUSER_INFO_1010, lmaccess/PUSER_INFO_1010, lmaccess/USER_INFO_1010, netmgmt.user_info_1010_str'
req.header: lmaccess.h
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
req.typenames: USER_INFO_1010, *PUSER_INFO_1010, *LPUSER_INFO_1010
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1010
 - lmaccess/_USER_INFO_1010
 - PUSER_INFO_1010
 - lmaccess/PUSER_INFO_1010
 - USER_INFO_1010
 - lmaccess/USER_INFO_1010
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_INFO_1010
---

# USER_INFO_1010 structure


## -description

The
				<b>USER_INFO_1010</b> structure contains a set of bit flags defining the operator privileges assigned to a user network account. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1010_auth_flags

Specifies a <b>DWORD</b> value that contains a set of bit flags that specify the user's operator privileges. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_OP_PRINT"></a><a id="af_op_print"></a><dl>
<dt><b>AF_OP_PRINT</b></dt>
</dl>
</td>
<td width="60%">
The print operator privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_OP_COMM"></a><a id="af_op_comm"></a><dl>
<dt><b>AF_OP_COMM</b></dt>
</dl>
</td>
<td width="60%">
The communications operator privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_OP_SERVER"></a><a id="af_op_server"></a><dl>
<dt><b>AF_OP_SERVER</b></dt>
</dl>
</td>
<td width="60%">
The server operator privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_OP_ACCOUNTS"></a><a id="af_op_accounts"></a><dl>
<dt><b>AF_OP_ACCOUNTS</b></dt>
</dl>
</td>
<td width="60%">
The accounts operator privilege is enabled.

</td>
</tr>
</table>

## -remarks

 For more information about controlling access to securable objects, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>, <a href="/windows/desktop/SecAuthZ/privileges">Privileges</a>, and <a href="/windows/desktop/SecAuthZ/securable-objects">Securable Objects</a>.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>