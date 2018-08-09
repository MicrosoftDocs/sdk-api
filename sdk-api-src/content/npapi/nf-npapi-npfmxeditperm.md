---
UID: NF:npapi.NPFMXEditPerm
title: NPFMXEditPerm function
author: windows-sdk-content
description: Enables network vendors to supply their own permission editor dialog boxes.
old-location: security\npfmxeditperm.htm
old-project: secauthn
ms.assetid: 72ea90ce-3493-49bf-beaa-833217495e47
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NPFMXEditPerm, NPFMXEditPerm function [Security], WNPERM_DLG_AUDIT, WNPERM_DLG_OWNER, WNPERM_DLG_PERM, _mnp_npfmxeditperm, npapi/NPFMXEditPerm, security.npfmxeditperm
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: NOTIFICATION_USER_INPUT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPFMXEditPerm
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set extended error information, which may include the following values.

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

<a href="https://msdn.microsoft.com/72ea90ce-3493-49bf-beaa-833217495e47">NPFMXEditPerm</a> is not supported in the provider.

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
 



