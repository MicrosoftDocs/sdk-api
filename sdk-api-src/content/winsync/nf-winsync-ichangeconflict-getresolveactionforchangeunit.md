---
UID: NF:winsync.IChangeConflict.GetResolveActionForChangeUnit
title: IChangeConflict::GetResolveActionForChangeUnit
author: windows-driver-content
description: Gets the conflict resolution action for the conflicting change unit change.
old-location: winsync\ichangeconflict_getresolveactionforchangeunit.htm
old-project: winsync
ms.assetid: 206ee654-e8a6-4b71-b933-3380dc4ed0ad
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetResolveActionForChangeUnit, GetResolveActionForChangeUnit method [Windows Sync], GetResolveActionForChangeUnit method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetResolveActionForChangeUnit method, IChangeConflict.GetResolveActionForChangeUnit, IChangeConflict::GetResolveActionForChangeUnit, winsync.ichangeconflict_getresolveactionforchangeunit, winsync/IChangeConflict::GetResolveActionForChangeUnit
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IChangeConflict.GetResolveActionForChangeUnit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeConflict::GetResolveActionForChangeUnit


## -description


Gets the conflict resolution action for the conflicting change unit change.


## -parameters




### -param pChangeUnit [in]

The change unit for which to retrieve the conflict resolution action.


### -param pResolveAction [out]

The conflict resolution action that is specified for <i>pChangeUnit</i>.


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
 

 

