---
UID: NF:winsync.IChangeConflict.GetDestinationProviderConflictingChange
title: IChangeConflict::GetDestinationProviderConflictingChange
author: windows-sdk-content
description: Gets the change metadata from the destination provider.
old-location: winsync\ichangeconflict_getdestinationproviderconflictingchange.htm
old-project: winsync
ms.assetid: 4624f92a-8455-4490-a256-9cf849626844
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetDestinationProviderConflictingChange, GetDestinationProviderConflictingChange method [Windows Sync], GetDestinationProviderConflictingChange method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetDestinationProviderConflictingChange method, IChangeConflict.GetDestinationProviderConflictingChange, IChangeConflict::GetDestinationProviderConflictingChange, winsync.ichangeconflict_getdestinationproviderconflictingchange, winsync/IChangeConflict::GetDestinationProviderConflictingChange
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
 - IChangeConflict.GetDestinationProviderConflictingChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeConflict::GetDestinationProviderConflictingChange


## -description


Gets the change metadata from the destination provider.


## -parameters




### -param ppConflictingChange [out]

Returns the change metadata from the destination provider.


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
<dt><b>SYNC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The change from the destination provider does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>
 

 

