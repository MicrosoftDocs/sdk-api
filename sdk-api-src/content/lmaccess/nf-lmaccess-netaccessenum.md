---
UID: NF:lmaccess.NetAccessEnum
title: NetAccessEnum function (lmaccess.h)
description: Not supported. (NetAccessEnum)
helpviewer_keywords: ["0","1","NetAccessEnum","NetAccessEnum function [Network Management]","_win32_netaccessenum","lmaccess/NetAccessEnum","netmgmt.netaccessenum"]
old-location: netmgmt\netaccessenum.htm
tech.root: NetMgmt
ms.assetid: 34ffea84-ff41-43c3-864c-957178e9d22a
ms.date: 12/05/2018
ms.keywords: 0, 1, NetAccessEnum, NetAccessEnum function [Network Management], _win32_netaccessenum, lmaccess/NetAccessEnum, netmgmt.netaccessenum
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
 - NetAccessEnum
 - lmaccess/NetAccessEnum
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
 - NetAccessEnum
---

## -description

<p class="CCE_Message">[This function is obsolete. For a list of alternate functions, see <a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization Functions</a>.]

Not supported.

The <b>NetAccessEnum</b> function retrieves information about each access permission record.

## -parameters

### -param servername

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param BasePath

Pointer to a string that contains a base pathname for the resource. A <b>NULL</b> pointer or <b>NULL</b> string means no base path is to be used. The path can be specified as a universal naming convention (UNC) pathname.

### -param Recursive

Specifies a flag that enables or disables recursive searching.

If this parameter is equal to zero, the <b>NetAccessEnum</b> function returns entries for the resource named as the base path by the <i>pszBasePath</i> parameter, and for the resources directly below that base path.

If this parameter is nonzero, the function returns entries for all access control lists (ACLs) that have <i>pszBasePath</i> at the beginning of the resource name.

### -param level

Specifies the information level of the data. This parameter can be one of the following values.

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
The <i>pbBuffer</i> parameter points to an 
<b>access_info_0</b> structure.

</td>
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

### -param bufptr

Pointer to the buffer that receives the access information structure. The format of this data depends on the value of the <i>sLevel</i> parameter.

### -param prefmaxlen

Specifies the size, in bytes, of the buffer pointed to by the <i>pbBuffer</i> parameter.

### -param entriesread

Pointer to an unsigned short integer that receives the count of elements actually enumerated. The count is valid only if the 
<b>NetAccessEnum</b> function returns <b>NERR_Success</b> or <b>ERROR_MORE_DATA</b>.

### -param totalentries

Pointer to an unsigned short integer that receives the total number of entries that could have been enumerated. The count is valid only if the 
<b>NetAccessEnum</b> function returns <b>NERR_Success</b> or <b>ERROR_MORE_DATA</b>.

### -param resume_handle

TBD

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function requires Admin privilege to successfully execute on a computer that has local security enabled.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Authorization functions</a>
