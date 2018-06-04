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

# NPFMXGetPermHelp function


## -description


Retrieves the help file and help context of the permission editor dialog boxes when a menu item in the <b>Security</b> menu of File Manager is selected and F1 is pressed.


## -parameters




### -param lpDriveName [in]

Pointer to the name of the drive currently selected in File Manager.


### -param nDialogType

TBD


### -param fDirectory [in]

Specifies whether the selected item is a directory. This should be set to <b>TRUE</b> if the selected item in File Manager is a directory, and <b>FALSE</b> if it is a file.


### -param lpFileNameBuffer

TBD


### -param lpBufferSize [in, out]

Pointer to a <b>DWORD</b> that specifies the size of the buffer passed in. If <i>lpBuffer</i> is not large enough, on return, this contains the size of buffer needed.


### -param lpnHelpContext [out]

Pointer to a <b>DWORD</b> that will receive the help context for the given <i>nType</i>.


#### - lpBuffer [in, out]

Pointer to a buffer that will receive the help file name.


#### - nType [in]

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
The <a href="https://msdn.microsoft.com/a7bf24fb-a775-4a13-a808-86a0d4d25332">NPFMXGetPermHelp</a> function is not supported in the provider.

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
 



