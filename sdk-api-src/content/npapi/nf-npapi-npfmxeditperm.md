---
UID: NF:npapi.NPFMXEditPerm
title: NPFMXEditPerm function (npapi.h)
description: Enables network vendors to supply their own permission editor dialog boxes.
helpviewer_keywords: ["NPFMXEditPerm","NPFMXEditPerm function [Security]","WNPERM_DLG_AUDIT","WNPERM_DLG_OWNER","WNPERM_DLG_PERM","_mnp_npfmxeditperm","npapi/NPFMXEditPerm","security.npfmxeditperm"]
old-location: security\npfmxeditperm.htm
tech.root: security
ms.assetid: 72ea90ce-3493-49bf-beaa-833217495e47
ms.date: 12/05/2018
ms.keywords: NPFMXEditPerm, NPFMXEditPerm function [Security], WNPERM_DLG_AUDIT, WNPERM_DLG_OWNER, WNPERM_DLG_PERM, _mnp_npfmxeditperm, npapi/NPFMXEditPerm, security.npfmxeditperm
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
 - NPFMXEditPerm
 - npapi/NPFMXEditPerm
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
 - NPFMXEditPerm
---

# NPFMXEditPerm function


## -description

Enables network vendors to supply their own permission editor dialog boxes.

## -parameters

### -param lpDriveName [in]

Pointer to the current drive name selected in File Manager.

### -param hwndFMX [in]

A handle to the FMX window which can be used to query selections.

### -param nDialogType [in]

Specifies the type of permission dialog box to bring up. This parameter can be one of the following values.

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
Brings up the <b>Permissions</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WNPERM_DLG_AUDIT"></a><a id="wnperm_dlg_audit"></a><dl>
<dt><b>WNPERM_DLG_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Brings up the <b>Auditing</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WNPERM_DLG_OWNER"></a><a id="wnperm_dlg_owner"></a><dl>
<dt><b>WNPERM_DLG_OWNER</b></dt>
</dl>
</td>
<td width="60%">
Brings up the <b>Owner</b> dialog box.

</td>
</tr>
</table>

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

<a href="/windows/desktop/api/npapi/nf-npapi-npfmxeditperm">NPFMXEditPerm</a> is not supported in the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Some parameter takes an unexpected form or value. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to display the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Some other network error occurred.

</td>
</tr>
</table>