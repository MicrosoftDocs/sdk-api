---
UID: NF:lmaccess.NetAccessGetUserPerms
title: NetAccessGetUserPerms function (lmaccess.h)
description: Not supported. (NetAccessGetUserPerms)
helpviewer_keywords: ["NetAccessGetUserPerms","NetAccessGetUserPerms function [Network Management]","_win32_netaccessgetuserperms","lmaccess/NetAccessGetUserPerms","netmgmt.netaccessgetuserperms"]
old-location: netmgmt\netaccessgetuserperms.htm
tech.root: NetMgmt
ms.assetid: 8f4f069f-86d7-40cf-a821-32345d308f70
ms.date: 12/05/2018
ms.keywords: NetAccessGetUserPerms, NetAccessGetUserPerms function [Network Management], _win32_netaccessgetuserperms, lmaccess/NetAccessGetUserPerms, netmgmt.netaccessgetuserperms
req.header: lmaccess.h
req.include-header: Lm.h, Lmaccess.h
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
 - NetAccessGetUserPerms
 - lmaccess/NetAccessGetUserPerms
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
 - NetAccessGetUserPerms
---

# NetAccessGetUserPerms function


## -description

<p class="CCE_Message">[This function is obsolete. For a list of alternate functions, see <a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization Functions</a>.]

Not supported.

 The 
<b>NetAccessGetUserPerms</b> function returns a specified user's or group's access permissions for a particular resource.

## -parameters

### -param servername

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param UGname

Pointer to a string that specifies the name of the user or group to query.

### -param resource

Pointer to a string that contains the name of the network resource to query.

### -param Perms

Pointer to an unsigned short integer that receives the user permissions for the specified resource.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function requires Admin privilege to successfully execute on a computer that has local security enabled. When users request their own access permissions, no special privilege is required.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization Functions</a>
