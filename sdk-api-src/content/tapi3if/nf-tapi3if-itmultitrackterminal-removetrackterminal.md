---
UID: NF:tapi3if.ITMultiTrackTerminal.RemoveTrackTerminal
title: ITMultiTrackTerminal::RemoveTrackTerminal
author: windows-sdk-content
description: The RemoveTrackTerminal method removes the specified terminal from the collection of track terminals that belong to the multitrack terminal on which the method was called.
old-location: tapi3\itmultitrackterminal_removetrackterminal.htm
old-project: tapi
ms.assetid: 59f257ef-9e52-40fb-a72c-732105262016
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITMultiTrackTerminal interface [TAPI 2.2],RemoveTrackTerminal method, ITMultiTrackTerminal.RemoveTrackTerminal, ITMultiTrackTerminal::RemoveTrackTerminal, RemoveTrackTerminal, RemoveTrackTerminal method [TAPI 2.2], RemoveTrackTerminal method [TAPI 2.2],ITMultiTrackTerminal interface, _tapi3_itmultitrackterminal_removetrackterminal, tapi3.itmultitrackterminal_removetrackterminal, tapi3if/ITMultiTrackTerminal::RemoveTrackTerminal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMultiTrackTerminal.RemoveTrackTerminal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMultiTrackTerminal::RemoveTrackTerminal


## -description


The 
<b>RemoveTrackTerminal</b> method removes the specified terminal from the collection of track terminals that belong to the multitrack terminal on which the method was called. If the track terminal has been selected on a stream, it should be unselected first.


## -parameters




### -param pTrackTerminalToRemove [in]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface of the terminal to remove.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTrackTerminalToRemove</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The primary use of the 
<b>RemoveTrackTerminal</b> method is cleanup during the terminal selection process. For example, if a track has been created, but it has not been selected on a stream, this method can be used to remove the track.

The actual action performed by this method may vary in the actual implementation of the terminal. For instance, calling this method on a File Recording Terminal causes the corresponding file data stream to be removed from the file. Calling this method on a File Playback Terminal fails because its set of terminals is determined solely by file configuration and cannot be changed by the caller.




## -see-also




<a href="https://msdn.microsoft.com/c9e5d8a4-78a6-4449-9c11-c780e72ab925">ITMultiTrackTerminal</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 

