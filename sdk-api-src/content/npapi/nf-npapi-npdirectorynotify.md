---
UID: NF:npapi.NPDirectoryNotify
title: NPDirectoryNotify function (npapi.h)
description: Notifies the network provider of certain directory operations.
helpviewer_keywords: ["NPDirectoryNotify","NPDirectoryNotify function [Security]","WNDN_MKDIR","WNDN_MVDIR","WNDN_RMDIR","_mnp_npdirectorynotify","npapi/NPDirectoryNotify","security.npdirectorynotify"]
old-location: security\npdirectorynotify.htm
tech.root: security
ms.assetid: e76642b1-4af1-46f4-92c0-f10ff57dd808
ms.date: 12/05/2018
ms.keywords: NPDirectoryNotify, NPDirectoryNotify function [Security], WNDN_MKDIR, WNDN_MVDIR, WNDN_RMDIR, _mnp_npdirectorynotify, npapi/NPDirectoryNotify, security.npdirectorynotify
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
 - NPDirectoryNotify
 - npapi/NPDirectoryNotify
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
 - NPDirectoryNotify
---

# NPDirectoryNotify function


## -description

 Notifies the network provider of certain directory operations. The <b>NPDirectoryNotify</b> function is used by File Manager. This function can be used to perform special operations on certain directories.

## -parameters

### -param hwnd [in]

A handle to a window that should own any messages or dialog boxes in the event the network provider needs to interact with the user.

### -param lpDir [in]

Pointer to the fully qualified name of the directory.

### -param dwOper [in]

Indicates the operation about to be performed. This can be one of the following values. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNDN_MKDIR"></a><a id="wndn_mkdir"></a><dl>
<dt><b>WNDN_MKDIR</b></dt>
</dl>
</td>
<td width="60%">
File Manager is about to create a directory with the given name.

</td>
</tr>
<tr>
<td width="40%"><a id="WNDN_RMDIR"></a><a id="wndn_rmdir"></a><dl>
<dt><b>WNDN_RMDIR</b></dt>
</dl>
</td>
<td width="60%">
File Manager is about to remove the directory.

</td>
</tr>
<tr>
<td width="40%"><a id="WNDN_MVDIR"></a><a id="wndn_mvdir"></a><dl>
<dt><b>WNDN_MVDIR</b></dt>
</dl>
</td>
<td width="60%">
File Manager is about to rename the directory.

</td>
</tr>
</table>

## -returns

This function should return WN_SUCCESS if it is successful. This indicates to the caller that it should continue and perform the operation. Otherwise, it should return the appropriate code, which may include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The provider would have handled the operation, but the user canceled it. The caller should not perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CONTINUE</b></dt>
</dl>
</td>
<td width="60%">
The network provider has already handled the operation. The caller should proceed normally but should not perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The network does not have special directory handling. This is treated as WN_SUCCESS.

</td>
</tr>
</table>

