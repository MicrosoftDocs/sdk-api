---
UID: NF:npapi.NPFMXGetPermHelp
title: NPFMXGetPermHelp function (npapi.h)
description: Retrieves the help file and help context of the permission editor dialog boxes when a menu item in the Security menu of File Manager is selected and F1 is pressed.
helpviewer_keywords: ["NPFMXGetPermHelp","NPFMXGetPermHelp function [Security]","WNPERM_DLG_AUDIT","WNPERM_DLG_OWNER","WNPERM_DLG_PERM","_mnp_npfmxgetpermhelp","npapi/NPFMXGetPermHelp","security.npfmxgetpermhelp"]
old-location: security\npfmxgetpermhelp.htm
tech.root: security
ms.assetid: a7bf24fb-a775-4a13-a808-86a0d4d25332
ms.date: 12/05/2018
ms.keywords: NPFMXGetPermHelp, NPFMXGetPermHelp function [Security], WNPERM_DLG_AUDIT, WNPERM_DLG_OWNER, WNPERM_DLG_PERM, _mnp_npfmxgetpermhelp, npapi/NPFMXGetPermHelp, security.npfmxgetpermhelp
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
 - NPFMXGetPermHelp
 - npapi/NPFMXGetPermHelp
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
 - NPFMXGetPermHelp
---

# NPFMXGetPermHelp function


## -description

Retrieves the help file and help context of the permission editor dialog boxes when a menu item in the <b>Security</b> menu of File Manager is selected and F1 is pressed.

## -parameters

### -param lpDriveName [in]

Pointer to the name of the drive currently selected in File Manager.

### -param nDialogType [in]

Specifies the menu item in the <b>Security</b> menu of File Manager on which to bring up Help. This can be one of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNPERM_DLG_PERM"></a><a id="wnperm_dlg_perm"></a><dl>
<dt><b>WNPERM_DLG_PERM</b></dt>
</dl>
</td>
<td width="60%">
Show help on the <b>Permissions</b> menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="WNPERM_DLG_AUDIT"></a><a id="wnperm_dlg_audit"></a><dl>
<dt><b>WNPERM_DLG_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Show help on the <b>Auditing</b> menu item. 

</td>
</tr>
<tr>
<td width="40%"><a id="WNPERM_DLG_OWNER"></a><a id="wnperm_dlg_owner"></a><dl>
<dt><b>WNPERM_DLG_OWNER</b></dt>
</dl>
</td>
<td width="60%">
Show help on the <b>Owner</b> menu item.

</td>
</tr>
</table>

### -param fDirectory [in]

Specifies whether the selected item is a directory. This should be set to <b>TRUE</b> if the selected item in File Manager is a directory, and <b>FALSE</b> if it is a file.

### -param lpFileNameBuffer [in, out]

Pointer to a buffer that will receive the help file name.

### -param lpBufferSize [in, out]

Pointer to a <b>DWORD</b> that specifies the size of the buffer passed in. If <i>lpBuffer</i> is not large enough, on return, this contains the size of buffer needed.

### -param lpnHelpContext [out]

Pointer to a <b>DWORD</b> that will receive the help context for the given <i>nType</i>.

## -returns

If the function succeeds, the function should return WN_SUCCESS.

If the function fails, it should call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to set extended error information, which may include the following values.
					

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
The <a href="/windows/desktop/api/npapi/nf-npapi-npfmxgetpermhelp">NPFMXGetPermHelp</a> function is not supported in the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters is an unexpected form or value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer is too small.

</td>
</tr>
</table>