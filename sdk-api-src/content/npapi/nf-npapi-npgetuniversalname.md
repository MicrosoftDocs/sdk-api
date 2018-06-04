---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NPGetUniversalName function


## -description


Retrieves the universal name of a network resource. The <b>NPGetUniversalName</b> function can retrieve this universal name in UNC format or in the older, remote-name format.


## -parameters




### -param lpLocalPath [in]

Pointer to the local path of an object on a network resource. This is a drive-based path.


### -param dwInfoLevel [in]

The level of detail of information the caller is interested in. This can be one of the following values. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UNIVERSAL_NAME_INFO_LEVEL"></a><a id="universal_name_info_level"></a><dl>
<dt><b>UNIVERSAL_NAME_INFO_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the UNC form of the name, for example: "file:\\server\share" 




If this value is set, the data returned in <i>lpBuffer</i> is stored as a 
<a href="https://msdn.microsoft.com/505bcd3e-4043-4856-9a6f-a6f074dc6076">UNIVERSAL_NAME_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="REMOTE_NAME_INFO_LEVEL"></a><a id="remote_name_info_level"></a><dl>
<dt><b>REMOTE_NAME_INFO_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the remote form of the name, for example: "\\server\share" 




If this value is set, the data returned in <i>lpBuffer</i> is stored as a 
<a href="https://msdn.microsoft.com/5dec0c40-757e-4c3b-8442-23f6d0f0e670">REMOTE_NAME_INFO</a> structure.

</td>
</tr>
</table>
 


### -param lpBuffer [out]

Pointer to a buffer to receive the information the user has requested. The specific structure returned depends on the information level specified in <i>dwInfoLevel</i>.


### -param lpBufferSize [in, out]

Pointer to the size, in bytes, of the <i>lpBuffer</i> buffer. If the call fails because the buffer is not big enough, this location will be used to return the required buffer size.


## -returns



If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code, which may be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_LOCALNAME</b></dt>
</dl>
</td>
<td width="60%">
The value passed into <i>lpLocalPath</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The value passed into <i>lpLocalPath</i> is not a redirected device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present.

</td>
</tr>
</table>
 



