---
UID: NF:winsync.IChangeConflict.GetSourceProviderConflictingChange
title: IChangeConflict::GetSourceProviderConflictingChange
author: windows-sdk-content
description: Gets the change metadata from the source provider.
old-location: winsync\ichangeconflict_getsourceproviderconflictingchange.htm
old-project: winsync
ms.assetid: a77983ec-77fd-4e24-a978-df37a85b0ede
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSourceProviderConflictingChange, GetSourceProviderConflictingChange method [Windows Sync], GetSourceProviderConflictingChange method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetSourceProviderConflictingChange method, IChangeConflict.GetSourceProviderConflictingChange, IChangeConflict::GetSourceProviderConflictingChange, winsync.ichangeconflict_getsourceproviderconflictingchange, winsync/IChangeConflict::GetSourceProviderConflictingChange
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeConflict.GetSourceProviderConflictingChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeConflict::GetSourceProviderConflictingChange


## -description


Gets the change metadata from the source provider.


## -parameters




### -param ppConflictingChange






#### - ppSyncChange [out]

Returns the change metadata from the source provider.


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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INTERNAL_ERROR </b></dt>
</dl>
</td>
<td width="60%">
The change from the source provider does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>
 

 

