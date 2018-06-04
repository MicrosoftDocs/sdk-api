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

# ITransferAdviseSink::ConfirmOverwrite


## -description


Displays a message to the user confirming that overwriting existing items is acceptable.


## -parameters




### -param psiSource

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the source <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> .


### -param psiDestParent

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the destination parent folder <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param pszName

Type: <b>LPCWSTR</b>

A pointer to a wide-string containing the desired name of the item at the destination. If <b>NULL</b>, the name is the same as the Shell item pointed to by <i>psiSource</i>.


## -returns



Type: <b>HRESULT</b>

The return values listed below are emitted specifically by this method to inform the calling process of how the operation ended.  If other results or errors are emitted during the operation of this method, they should be returned to the calling process.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USER_IGNORED</b></dt>
</dl>
</td>
<td width="60%">
The user clicked <b>Ignore</b>. Allows the calling process to continue processing other files as appropriate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user clicked <b>Cancel</b>. Stops processing of the current document and ends the current process.

</td>
</tr>
</table>
 



