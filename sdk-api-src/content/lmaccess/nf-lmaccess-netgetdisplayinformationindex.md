---
UID: NF:lmaccess.NetGetDisplayInformationIndex
title: NetGetDisplayInformationIndex function (lmaccess.h)
description: The NetGetDisplayInformationIndex function returns the index of the first display information entry whose name begins with a specified string or whose name alphabetically follows the string.
helpviewer_keywords: ["1","2","3","NetGetDisplayInformationIndex","NetGetDisplayInformationIndex function [Network Management]","_win32_netgetdisplayinformationindex","lmaccess/NetGetDisplayInformationIndex","netmgmt.netgetdisplayinformationindex"]
old-location: netmgmt\netgetdisplayinformationindex.htm
tech.root: NetMgmt
ms.assetid: c56b3cf9-e0a2-4b66-a518-70753b79214c
ms.date: 12/05/2018
ms.keywords: 1, 2, 3, NetGetDisplayInformationIndex, NetGetDisplayInformationIndex function [Network Management], _win32_netgetdisplayinformationindex, lmaccess/NetGetDisplayInformationIndex, netmgmt.netgetdisplayinformationindex
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetGetDisplayInformationIndex
 - lmaccess/NetGetDisplayInformationIndex
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
 - NetGetDisplayInformationIndex
---

# NetGetDisplayInformationIndex function


## -description

The 
				<b>NetGetDisplayInformationIndex</b> function returns the index of the first display information entry whose name begins with a specified string or whose name alphabetically follows the string. You can use this function to determine a starting index for subsequent calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a> function.

## -parameters

### -param ServerName [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param Level [in]

Specifies the level of accounts to query. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Query all local and global (normal) user accounts.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Query all workstation and server user accounts.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Query all global groups.

</td>
</tr>
</table>

### -param Prefix [in]

Pointer to a string that specifies the prefix for which to search.

### -param Index [out]

Pointer to a value that receives the index of the requested entry.

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
The value specified for the <i>Level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There were no more items on which to operate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The computer name is invalid.

</td>
</tr>
</table>

## -remarks

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The function only returns information to which the caller has Read access. The caller must have List Contents access to the Domain object, and  Enumerate Entire SAM Domain access on the SAM Server object  located in the System container.

## -see-also

<a href="/windows/desktop/NetMgmt/get-functions">Get Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>