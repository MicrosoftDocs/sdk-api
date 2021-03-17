---
UID: NF:npapi.NPGetDirectoryType
title: NPGetDirectoryType function (npapi.h)
description: Determines the type of a network directory.
helpviewer_keywords: ["NPGetDirectoryType","NPGetDirectoryType function [Security]","_mnp_npgetdirectorytype","npapi/NPGetDirectoryType","security.npgetdirectorytype"]
old-location: security\npgetdirectorytype.htm
tech.root: security
ms.assetid: 70ee5c14-1395-470a-970c-91a3d3ac0fd1
ms.date: 12/05/2018
ms.keywords: NPGetDirectoryType, NPGetDirectoryType function [Security], _mnp_npgetdirectorytype, npapi/NPGetDirectoryType, security.npgetdirectorytype
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPGetDirectoryType
 - npapi/NPGetDirectoryType
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
 - NPGetDirectoryType
---

# NPGetDirectoryType function


## -description

Determines the type of a network directory. The <b>NPGetDirectoryType</b> function is used by File Manager.

## -parameters

### -param lpName [in]

Pointer to the fully qualified name of the directory. The network provider returns the type to the address pointed to by <i>lpType</i>. If the value returned in <i>lpType</i> is zero or if the network provider returns an error, File Manager displays the directory as a "normal" directory.

### -param lpType [in]

Pointer to a value defined by the network provider. This value is used to modify the display of the drive tree in File Manager. In this way, the network provider can show special directories to the user.

### -param bFlushCache [in]

Set to <b>TRUE</b> when File Manager calls MPR to get the directory type for the first time while repainting a window on Refresh. Subsequently, it will be <b>FALSE</b>. This gives a provider the opportunity to optimize performance if it wants to just read the data for a drive once and then cache it until the next Refresh.

## -returns

This function should return WN_SUCCESS if it is successful. Otherwise, it should return an error code, which may include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/npapi/nf-npapi-npgetdirectorytype">NPGetDirectoryType</a> is not supported.

</td>
</tr>
</table>

## -remarks

File Manager will supply its own icon for all special network directories; that is, when <i>lpType</i> is set to a nonzero value, File Manager will display a special folder icon.

The implementation of this function should be high-performance, or fast, since the call occurs while File Manager is painting the directory tree.