---
UID: NF:npapi.NPGetUniversalName
title: NPGetUniversalName function (npapi.h)
description: Retrieves the universal name of a network resource. The NPGetUniversalName function can retrieve this universal name in UNC format or in the older, remote-name format.
helpviewer_keywords: ["NPGetUniversalName","NPGetUniversalName function [Security]","REMOTE_NAME_INFO_LEVEL","UNIVERSAL_NAME_INFO_LEVEL","_mnp_npgetuniversalname","npapi/NPGetUniversalName","security.npgetuniversalname"]
old-location: security\npgetuniversalname.htm
tech.root: security
ms.assetid: 976b5910-c34f-49fa-b25e-82bf607e33a9
ms.date: 12/05/2018
ms.keywords: NPGetUniversalName, NPGetUniversalName function [Security], REMOTE_NAME_INFO_LEVEL, UNIVERSAL_NAME_INFO_LEVEL, _mnp_npgetuniversalname, npapi/NPGetUniversalName, security.npgetuniversalname
req.header: npapi.h
req.include-header: 
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
req.lib: davclnt.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPGetUniversalName
 - npapi/NPGetUniversalName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPGetUniversalName
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
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-universal_name_infoa">UNIVERSAL_NAME_INFO</a> structure.

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
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-remote_name_infoa">REMOTE_NAME_INFO</a> structure.

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