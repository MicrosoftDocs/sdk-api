---
UID: NF:winsync.ISyncChangeUnit.GetChangeUnitVersion
title: ISyncChangeUnit::GetChangeUnitVersion
author: windows-sdk-content
description: Gets the version for the change unit change.
old-location: winsync\isyncchangeunit_getchangeunitversion.htm
old-project: winsync
ms.assetid: b40ec132-0459-4ddf-9156-bce2a1dfbc4d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetChangeUnitVersion, GetChangeUnitVersion method [Windows Sync], GetChangeUnitVersion method [Windows Sync],ISyncChangeUnit interface, ISyncChangeUnit interface [Windows Sync],GetChangeUnitVersion method, ISyncChangeUnit.GetChangeUnitVersion, ISyncChangeUnit::GetChangeUnitVersion, winsync.isyncchangeunit_getchangeunitversion, winsync/ISyncChangeUnit::GetChangeUnitVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.redist: 
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
 - ISyncChangeUnit.GetChangeUnitVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeUnit::GetChangeUnitVersion


## -description


Gets the version for the change unit change.


## -parameters




### -param pbCurrentReplicaId [in]

The ID of the replica that originated the change to retrieve.


### -param pVersion [out]

Returns the version of the change.


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
<i>pbCurrentReplicaId</i> is not the correct replica ID.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c889a78-1a50-47b5-8e49-4aba741c0be0">ISyncChangeUnit Interface</a>



<a href="https://msdn.microsoft.com/6a493a58-3dab-4032-90de-be9f903ae489">SYNC_VERSION Structure</a>
 

 

