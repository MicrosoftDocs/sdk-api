---
UID: NF:winnetwk.WNetGetResourceInformationA
title: WNetGetResourceInformationA function (winnetwk.h)
description: When provided with a remote path to a network resource, the WNetGetResourceInformation function identifies the network provider that owns the resource and obtains information about the type of the resource. (ANSI)
helpviewer_keywords: ["WNetGetResourceInformationA", "winnetwk/WNetGetResourceInformationA"]
old-location: wnet\wnetgetresourceinformation.htm
tech.root: WNet
ms.assetid: 19273874-adf1-4ffb-8b83-0eaa64e4622e
ms.date: 12/05/2018
ms.keywords: WNetGetResourceInformation, WNetGetResourceInformation function [Windows Networking (WNet)], WNetGetResourceInformationA, WNetGetResourceInformationW, _win32_wnetgetresourceinformation, winnetwk/WNetGetResourceInformation, winnetwk/WNetGetResourceInformationA, winnetwk/WNetGetResourceInformationW, wnet.wnetgetresourceinformation
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetResourceInformationW (Unicode) and WNetGetResourceInformationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNetGetResourceInformationA
 - winnetwk/WNetGetResourceInformationA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetGetResourceInformation
 - WNetGetResourceInformationA
 - WNetGetResourceInformationW
---

# WNetGetResourceInformationA function


## -description

When provided with a remote path to a network resource, the 
<b>WNetGetResourceInformation</b> function identifies the network provider that owns the resource and obtains information about the type of the resource. The function is typically used in conjunction with the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetresourceparenta">WNetGetResourceParent</a> function to parse and interpret a network path typed in by a user.

## -parameters

### -param lpNetResource [in]

Pointer to a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure that specifies the network resource for which information is required. 




The <b>lpRemoteName</b> member of the structure should specify the remote path name of the resource, typically one typed in by a user. The <b>lpProvider</b> and <b>dwType</b> members should also be filled in if known, because this operation can be memory intensive, especially if you do not specify the <b>dwType</b> member. If you do not know the values for these members, you should set them to <b>NULL</b>. All other members of the 
<b>NETRESOURCE</b> structure are ignored.

### -param lpBuffer [out]

Pointer to the buffer to receive the result. On successful return, the first portion of the buffer is a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure representing that portion of the input resource path that is accessed through the WNet functions, rather than through system functions specific to the input resource type. (The remainder of the buffer contains the variable-length strings to which the members of the 
<b>NETRESOURCE</b> structure point.) 




For example, if the input remote resource path is \\server\share\dir1\dir2, then the output 
<b>NETRESOURCE</b> structure contains information about the resource \\server\share. The \dir1\dir2 portion of the path is accessed through the 
<a href="/windows/desktop/FileIO/file-management-functions">file management functions</a>. The <b>lpRemoteName</b>, <b>lpProvider</b>, <b>dwType</b>, <b>dwDisplayType</b>, and <b>dwUsage</b> members of 
<b>NETRESOURCE</b> are returned, with all other members set to <b>NULL</b>.

The <b>lpRemoteName</b> member is returned in the same syntax as the one returned from an enumeration by the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a> function. This allows the caller to perform a string comparison to determine whether the resource passed to 
<b>WNetGetResourceInformation</b> is the same as the resource returned by a separate call to 
<b>WNetEnumResource</b>.

### -param lpcbBuffer [in, out]

Pointer to a location that, on entry, specifies the size of the <i>lpBuffer</i> buffer, in bytes. The buffer you allocate must be large enough to hold the 
<b>NETRESOURCE</b> structure, plus the strings to which its members point. If the buffer is too small for the result, this location receives the required buffer size, and the function returns ERROR_MORE_DATA.

### -param lplpSystem [out]

If the function returns successfully, this parameter points to a string in the output buffer that specifies the part of the resource that is accessed through system functions. (This applies only to functions specific to the resource type rather than the WNet functions.) 




For example, if the input remote resource name is \\server\share\dir1\dir2, the <b>lpRemoteName</b> member of the output 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure points to \\server\share. Also, the <i>lplpSystem</i> parameter points to \dir1\dir2. Both strings are stored in the buffer pointed to by the <i>lpBuffer</i> parameter.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NET_NAME</b></dt>
</dl>
</td>
<td width="60%">
The input <b>lpRemoteName</b> member is not an existing network resource for any network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEV_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The input <b>dwType</b> member does not match the type of resource specified by the <b>lpRemoteName</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Call 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> to obtain a description of the error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>lpBuffer</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa">WNetGetNetworkInformation</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetprovidernamea">WNetGetProviderName</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetresourceparenta">WNetGetResourceParent</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea">WNetGetUniversalName</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>

## -remarks

> [!NOTE]
> The winnetwk.h header defines WNetGetResourceInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
