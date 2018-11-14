---
UID: NF:winsync.IChangeConflict.GetResolveActionForChange
title: IChangeConflict::GetResolveActionForChange
author: windows-sdk-content
description: Gets the conflict resolution action for the conflict.
old-location: winsync\ichangeconflict_getresolveactionforchange.htm
tech.root: winsync
ms.assetid: b89124fe-200e-4061-974e-2d686de7a932
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetResolveActionForChange, GetResolveActionForChange method [Windows Sync], GetResolveActionForChange method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetResolveActionForChange method, IChangeConflict.GetResolveActionForChange, IChangeConflict::GetResolveActionForChange, winsync.ichangeconflict_getresolveactionforchange, winsync/IChangeConflict::GetResolveActionForChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeConflict.GetResolveActionForChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- IChangeConflict.GetResolveActionForChange
: 
---

# IChangeConflict::GetResolveActionForChange


## -description


Gets the conflict resolution action for the conflict.


## -parameters




### -param pResolveAction [out]

Returns the conflict resolution action for the conflict.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>



<a href="https://msdn.microsoft.com/6549eee1-6bf4-46b0-97d1-bb2c0f1b59a4">SYNC RESOLVE ACTION Enumeration</a>
 

 

