---
UID: NF:winnetwk.WNetGetResourceInformationA
title: WNetGetResourceInformationA function
author: windows-sdk-content
description: When provided with a remote path to a network resource, the WNetGetResourceInformation function identifies the network provider that owns the resource and obtains information about the type of the resource.
old-location: wnet\wnetgetresourceinformation.htm
old-project: wnet
ms.assetid: 19273874-adf1-4ffb-8b83-0eaa64e4622e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WNetGetResourceInformation, WNetGetResourceInformation function [Windows Networking (WNet)], WNetGetResourceInformationA, WNetGetResourceInformationW, _win32_wnetgetresourceinformation, winnetwk/WNetGetResourceInformation, winnetwk/WNetGetResourceInformationA, winnetwk/WNetGetResourceInformationW, wnet.wnetgetresourceinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnetwk.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WINML_VARIABLE_DESC
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
product: Windows
targetos: Windows
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WNetGetResourceInformationA function


## -description


When provided with a remote path to a network resource, the 
<b>WNetGetResourceInformation</b> function identifies the network provider that owns the resource and obtains information about the type of the resource. The function is typically used in conjunction with the 
<a href="https://msdn.microsoft.com/6ad5e2c0-d557-43cc-8ccf-a21160e262f8">WNetGetResourceParent</a> function to parse and interpret a network path typed in by a user.


## -parameters




### -param lpNetResource [in]

Pointer to a 
<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a> structure that specifies the network resource for which information is required. 




The <b>lpRemoteName</b> member of the structure should specify the remote path name of the resource, typically one typed in by a user. The <b>lpProvider</b> and <b>dwType</b> members should also be filled in if known, because this operation can be memory intensive, especially if you do not specify the <b>dwType</b> member. If you do not know the values for these members, you should set them to <b>NULL</b>. All other members of the 
<b>NETRESOURCE</b> structure are ignored.


### -param lpBuffer [out]

Pointer to the buffer to receive the result. On successful return, the first portion of the buffer is a 
<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a> structure representing that portion of the input resource path that is accessed through the WNet functions, rather than through system functions specific to the input resource type. (The remainder of the buffer contains the variable-length strings to which the members of the 
<b>NETRESOURCE</b> structure point.) 




For example, if the input remote resource path is \\server\share\dir1\dir2, then the output 
<b>NETRESOURCE</b> structure contains information about the resource \\server\share. The \dir1\dir2 portion of the path is accessed through the 
<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">file management functions</a>. The <b>lpRemoteName</b>, <b>lpProvider</b>, <b>dwType</b>, <b>dwDisplayType</b>, and <b>dwUsage</b> members of 
<b>NETRESOURCE</b> are returned, with all other members set to <b>NULL</b>.

The <b>lpRemoteName</b> member is returned in the same syntax as the one returned from an enumeration by the 
<a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a> function. This allows the caller to perform a string comparison to determine whether the resource passed to 
<b>WNetGetResourceInformation</b> is the same as the resource returned by a separate call to 
<b>WNetEnumResource</b>.


### -param lpcbBuffer [in, out]

Pointer to a location that, on entry, specifies the size of the <i>lpBuffer</i> buffer, in bytes. The buffer you allocate must be large enough to hold the 
<b>NETRESOURCE</b> structure, plus the strings to which its members point. If the buffer is too small for the result, this location receives the required buffer size, and the function returns ERROR_MORE_DATA.


### -param lplpSystem [out]

If the function returns successfully, this parameter points to a string in the output buffer that specifies the part of the resource that is accessed through system functions. (This applies only to functions specific to the resource type rather than the WNet functions.) 




For example, if the input remote resource name is \\server\share\dir1\dir2, the <b>lpRemoteName</b> member of the output 
<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a> structure points to \\server\share. Also, the <i>lplpSystem</i> parameter points to \dir1\dir2. Both strings are stored in the buffer pointed to by the <i>lpBuffer</i> parameter.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of the following values.

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
<a href="https://msdn.microsoft.com/8e13c467-adcf-4e97-b51a-1f5fc919b51e">WNetGetLastError</a> to obtain a description of the error.

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




<a href="https://msdn.microsoft.com/df190133-b73b-4f3e-aaee-4095cd619065">WNetGetNetworkInformation</a>



<a href="https://msdn.microsoft.com/c1369098-c574-4d5f-8051-ca5aa548e63f">WNetGetProviderName</a>



<a href="https://msdn.microsoft.com/6ad5e2c0-d557-43cc-8ccf-a21160e262f8">WNetGetResourceParent</a>



<a href="https://msdn.microsoft.com/12c02092-f2d5-4477-92a7-ae075b8a243a">WNetGetUniversalName</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

