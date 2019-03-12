---
UID: NF:lmaccess.NetAccessGetInfo
title: NetAccessGetInfo function
author: windows-sdk-content
description: Not supported.
old-location: netmgmt\netaccessgetinfo.htm
tech.root: NetMgmt
ms.assetid: 76d818db-ce13-4879-9ba5-c26d13fe098a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 0, 1, NetAccessGetInfo, NetAccessGetInfo function [Network Management], _win32_netaccessgetinfo, lmaccess/NetAccessGetInfo, netmgmt.netaccessgetinfo
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetAccessGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetAccessGetInfo function


## -description


<p class="CCE_Message">[This function is obsolete. For a list of alternate functions, see <a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Authorization Functions</a>.]

Not supported.

The <b>NetAccessGetInfo</b> function retrieves the access control list (ACL) for a specified resource.


## -parameters




### -param servername

TBD


### -param resource

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
The p parameter points to an 
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
 


### -param level

Pointer to the buffer that receives the access information structure. The format of this data depends on the value of the <i>sLevel</i> parameter.


### -param bufptr

Specifies the size, in bytes, of the buffer pointed to by the <i>pbBuffer</i> parameter.


#### - pcbTotalAvail

Pointer to an unsigned short integer that receives the total number of entries available. The count is valid only if the 
<b>NetAccessGetInfo</b> function returns <b>NERR_Success</b>, <b>NERR_BufTooSmall</b>, or <b>ERROR_MORE_DATA</b>.


#### - pszServer

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



This function requires Admin privilege to successfully execute on a computer that has local security enabled.




## -see-also




<a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Authorization Functions</a>
 

 

