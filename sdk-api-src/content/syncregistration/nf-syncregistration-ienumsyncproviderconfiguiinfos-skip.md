---
UID: NF:syncregistration.IEnumSyncProviderConfigUIInfos.Skip
title: IEnumSyncProviderConfigUIInfos::Skip
author: windows-sdk-content
description: Skips the specified number of ISyncProviderConfigUIInfo objects.
old-location: winsync\ienumsyncproviderconfiguiinfos_skip.htm
old-project: winsync
ms.assetid: 7ecd6cce-77af-423a-9b95-80b1d7ec9d2f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumSyncProviderConfigUIInfos interface [Windows Sync],Skip method, IEnumSyncProviderConfigUIInfos.Skip, IEnumSyncProviderConfigUIInfos::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumSyncProviderConfigUIInfos interface, syncregistration/IEnumSyncProviderConfigUIInfos::Skip, winsync.ienumsyncproviderconfiguiinfos_skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncregistration.h
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
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - IEnumSyncProviderConfigUIInfos.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumSyncProviderConfigUIInfos::Skip


## -description


Skips the specified number of <b>ISyncProviderConfigUIInfo</b> objects.


## -parameters




### -param cFactories [in]

The number of <b>ISyncProviderConfigUIInfo</b> objects to skip.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The end of the collection was reached before the specified number of items was skipped.

</td>
</tr>
</table>
 




## -remarks



If the end of the collection is reached before the number of items to skip is reached, <b>S_FALSE</b> will be returned, and the enumerator will be placed at the end of the collection and subsequent calls to <b>Skip</b> or <a href="https://msdn.microsoft.com/46564ed2-233d-409c-a996-dd3d9cfde907">Next</a> with a count of 1 will return <b>S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/d8b4f4a4-b238-431f-a123-edebe07ea7b0">IEnumSyncProviderConfigUIInfos Interface</a>
 

 

