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

# NPFMXEditPerm function


## -description


Enables network vendors to supply their own permission editor dialog boxes.


## -parameters




### -param lpDriveName [in]

Pointer to the current drive name selected in File Manager.


### -param hwndFMX [in]

A handle to the FMX window which can be used to query selections.


### -param nDialogType

TBD




#### - nType [in]

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
 



