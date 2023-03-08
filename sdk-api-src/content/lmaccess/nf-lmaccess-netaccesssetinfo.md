---
UID: NF:lmaccess.NetAccessSetInfo
title: NetAccessSetInfo function (lmaccess.h)
description: Not supported. (NetAccessSetInfo)
helpviewer_keywords: ["1","NetAccessSetInfo","NetAccessSetInfo function [Network Management]","_win32_netaccesssetinfo","lmaccess/NetAccessSetInfo","netmgmt.netaccesssetinfo"]
old-location: netmgmt\netaccesssetinfo.htm
tech.root: NetMgmt
ms.assetid: 9daf70e0-2402-4823-9e17-4702bbb3aa3d
ms.date: 12/05/2018
ms.keywords: 1, NetAccessSetInfo, NetAccessSetInfo function [Network Management], _win32_netaccesssetinfo, lmaccess/NetAccessSetInfo, netmgmt.netaccesssetinfo
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
 - NetAccessSetInfo
 - lmaccess/NetAccessSetInfo
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
 - NetAccessSetInfo
---

## -description

<p class="CCE_Message">[This function is obsolete. For a list of alternate functions, see <a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization Functions</a>.]

Not supported.

The <b>NetAccessSetInfo</b> function changes the access control list (ACL) for a resource.

## -parameters

### -param servername

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param resource

Pointer to a string that contains the name of the network resource to modify.

### -param level

Specifies the information level of the data. This parameter can be the following value.

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
The <i>pbBuffer</i> parameter points to an 
<b>access_info_1</b> structure.

</td>
</tr>
</table>

### -param buf

Pointer to the buffer that contains the access information structure. The format of this data depends on the value of the <i>sLevel</i> parameter.

### -param parm_err

TBD

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function requires Admin privilege to successfully execute on a computer that has local security enabled.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization functions</a>
