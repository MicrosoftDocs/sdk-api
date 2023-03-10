---
UID: NF:lmshare.NetFileGetInfo
title: NetFileGetInfo function (lmshare.h)
description: Retrieves information about a particular opening of a server resource.
helpviewer_keywords: ["2","3","NetFileGetInfo","NetFileGetInfo function [Files]","_win32_netfilegetinfo","fs.netfilegetinfo","lmshare/NetFileGetInfo","netmgmt.netfilegetinfo"]
old-location: fs\netfilegetinfo.htm
tech.root: fs
ms.assetid: d50c05e7-7ddd-4a7d-96f6-51878e52373c
ms.date: 12/05/2018
ms.keywords: 2, 3, NetFileGetInfo, NetFileGetInfo function [Files], _win32_netfilegetinfo, fs.netfilegetinfo, lmshare/NetFileGetInfo, netmgmt.netfilegetinfo
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
 - NetFileGetInfo
 - lmshare/NetFileGetInfo
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
 - NetFileGetInfo
---

# NetFileGetInfo function


## -description

Retrieves information about a particular opening of a server resource.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.

### -param fileid [in]

Specifies the file identifier of the open resource for which to return information. The value of this parameter must have been returned in a previous enumeration call. For more information, see the following Remarks section.

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
Return the file identification number. The <i>bufptr</i> parameter is a pointer to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_2">FILE_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return the file identification number and other information about the file. The <i>bufptr</i> parameter is a pointer to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_3">FILE_INFO_3</a> structure.

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the address of the buffer that receives the information. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file was not found.

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
<b>NetFileGetInfo</b> function.

You can call the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netfileenum">NetFileEnum</a> function to retrieve information about multiple files open on a server.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling 
<b>NetFileGetInfo</b>. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsresource">IADsResource</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>.

## -see-also

<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_2">FILE_INFO_2</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_3">FILE_INFO_3</a>



<a href="/windows/desktop/NetShare/netfile-functions">NetFile
		  Functions</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netfileenum">NetFileEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>