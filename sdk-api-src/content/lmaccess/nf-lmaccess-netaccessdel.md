---
UID: NF:lmaccess.NetAccessDel
title: NetAccessDel function (lmaccess.h)
description: Not supported. (NetAccessDel)
helpviewer_keywords: ["NetAccessDel","NetAccessDel function [Network Management]","_win32_netaccessdel","lmaccess/NetAccessDel","netmgmt.netaccessdel"]
old-location: netmgmt\netaccessdel.htm
tech.root: NetMgmt
ms.assetid: be33d9b4-9740-4ccb-ac95-25ae02edaa42
ms.date: 12/05/2018
ms.keywords: NetAccessDel, NetAccessDel function [Network Management], _win32_netaccessdel, lmaccess/NetAccessDel, netmgmt.netaccessdel
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
 - NetAccessDel
 - lmaccess/NetAccessDel
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
 - NetAccessDel
---

# NetAccessDel function


## -description

<p class="CCE_Message">[This function is obsolete. For a list of alternate functions, see <a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization Functions</a>.]

Not supported.

 The 
<b>NetAccessDel</b> function deletes the access control list (ACL) for a resource.

## -parameters

### -param servername

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param resource

Pointer to a string that contains the name of the network resource for which to remove the access control list.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function requires Admin privilege to successfully execute on a computer that has local security enabled.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization Functions</a>
