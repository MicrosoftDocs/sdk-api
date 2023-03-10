---
UID: NF:lmshare.NetFileEnum
title: NetFileEnum function (lmshare.h)
description: Returns information about some or all open files on a server, depending on the parameters specified.
helpviewer_keywords: ["2","3","NetFileEnum","NetFileEnum function [Files]","_win32_netfileenum","fs.netfileenum","lmshare/NetFileEnum","netmgmt.netfileenum"]
old-location: fs\netfileenum.htm
tech.root: fs
ms.assetid: 1375b337-efb0-4be1-94f7-473456a825b5
ms.date: 12/05/2018
ms.keywords: 2, 3, NetFileEnum, NetFileEnum function [Files], _win32_netfileenum, fs.netfileenum, lmshare/NetFileEnum, netmgmt.netfileenum
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - NetFileEnum
 - lmshare/NetFileEnum
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
 - NetFileEnum
---

# NetFileEnum function


## -description

Returns information about some or all open files on a server, depending on the parameters specified.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.

### -param basepath [in]

Pointer to a string that specifies a qualifier for the returned information. If this parameter is <b>NULL</b>, all open resources are enumerated. If this parameter is not <b>NULL</b>, the function enumerates only resources that have the value of the <i>basepath</i> parameter as a prefix. (A prefix is the portion of a path that comes before a backslash.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.

### -param username [in]

Pointer to a string that specifies the name of the user or the name of the connection. If the string begins with two backslashes ("\\"), then it indicates the name of the connection, for example, "\\127.0.0.1" or "\\ClientName". The part of the connection name after the backslashes is the same as the client name in the session information structure returned by the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a> function. If the string does not begin with two backslashes, then it indicates the name of the user. If this parameter is not <b>NULL</b>, its value serves as a qualifier for the enumeration. The files returned are limited to those that have user names or connection names that match the qualifier. If this parameter is <b>NULL</b>, no user-name qualifier is used.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This parameter is a pointer to a string that specifies the name of the user. If this parameter is not <b>NULL</b>, its value serves as a qualifier for the enumeration. The files returned are limited to those that have user names matching the qualifier. If this parameter is <b>NULL</b>, no user-name qualifier is used.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
 Return the file identification number. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_2">FILE_INFO_2</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
 Return information about the file. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_3">FILE_INFO_3</a> structures.

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the address of the buffer that receives the information. The format of this data depends on the value of the <i>level</i> parameter. 




This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with <b>ERROR_MORE_DATA</b>.

### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify <b>MAX_PREFERRED_LENGTH</b>, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns <b>ERROR_MORE_DATA</b>. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.

### -param resume_handle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing file search. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, no resume handle is stored.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

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
The value specified for the <i>level</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BufTooSmall</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is too small.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetFileEnum</b> function.

You can call the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo">NetFileGetInfo</a> function to retrieve information about a particular opening of a server resource.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling 
<b>NetFileEnum</b>. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsresource">IADsResource</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>.

## -see-also

<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_2">FILE_INFO_2</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_3">FILE_INFO_3</a>



<a href="/windows/desktop/NetShare/netfile-functions">NetFile
		  Functions</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo">NetFileGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>