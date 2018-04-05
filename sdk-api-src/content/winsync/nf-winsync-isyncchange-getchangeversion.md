---
UID: NF:winsync.ISyncChange.GetChangeVersion
title: ISyncChange::GetChangeVersion method
author: windows-driver-content
description: Gets the version that is associated with this change.
old-location: winsync\isyncchange_getchangeversion.htm
old-project: winsync
ms.assetid: 6b6def94-8c48-41f6-8869-e28d0db0d500
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetChangeVersion method [Windows Sync], GetChangeVersion method [Windows Sync], ISyncChange interface, GetChangeVersion,ISyncChange.GetChangeVersion, ISyncChange, ISyncChange interface [Windows Sync], GetChangeVersion method, ISyncChange::GetChangeVersion, winsync.isyncchange_getchangeversion, winsync/ISyncChange::GetChangeVersion
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
-	ISyncChange.GetChangeVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChange::GetChangeVersion method


## -description


Gets the version that is associated with this change.


## -parameters




### -param pbCurrentReplicaId [in]

The ID of the replica that owns this change. The ID format must match the format that is specified by the <a href="https://msdn.microsoft.com/7391689a-5546-409a-9fff-2ceced1850fe">ID_PARAMETERS</a> property of the provider.


### -param pVersion [out]

Returns the change version of the item.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i> pbCurrentReplicaId</i> is not the correct replica ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ITEM_HAS_NO_VERSION_DATA</b></dt>
</dl>
</td>
<td width="60%">
The item has been forgotten.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<i> pbCurrentReplicaId</i> is not in the format that is specified by the ID format schema of the provider.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ITEM_HAS_CHANGE_UNITS</b></dt>
</dl>
</td>
<td width="60%">
The item has change units.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange Interface</a>



<a href="https://msdn.microsoft.com/6a493a58-3dab-4032-90de-be9f903ae489">SYNC VERSION Structure</a>
 

 

