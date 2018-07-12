---
UID: NS:lmaccess._USER_INFO_1010
title: "_USER_INFO_1010"
author: windows-sdk-content
description: The USER_INFO_1010 structure contains a set of bit flags defining the operator privileges assigned to a user network account. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1010_str.htm
old-project: netmgmt
ms.assetid: 6760729a-1d59-430e-8412-1257977af169
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*LPUSER_INFO_1010, *PUSER_INFO_1010, AF_OP_ACCOUNTS, AF_OP_COMM, AF_OP_PRINT, AF_OP_SERVER, LPUSER_INFO_1010, LPUSER_INFO_1010 structure pointer [Network Management], PUSER_INFO_1010, PUSER_INFO_1010 structure pointer [Network Management], USER_INFO_1010, USER_INFO_1010 structure [Network Management], _USER_INFO_1010, _win32_user_info_1010_str, lmaccess/LPUSER_INFO_1010, lmaccess/PUSER_INFO_1010, lmaccess/USER_INFO_1010, netmgmt.user_info_1010_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: USER_INFO_1010, *PUSER_INFO_1010, *LPUSER_INFO_1010
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_INFO_1010
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_INFO_1010 structure


## -description


The
				<b>USER_INFO_1010</b> structure contains a set of bit flags defining the operator privileges assigned to a user network account. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


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



 For more information about controlling access to securable objects, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">Privileges</a>, and <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">Securable Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

