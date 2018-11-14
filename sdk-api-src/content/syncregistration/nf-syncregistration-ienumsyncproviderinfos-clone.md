---
UID: NF:syncregistration.IEnumSyncProviderInfos.Clone
title: IEnumSyncProviderInfos::Clone
author: windows-sdk-content
description: Clones the enumerator and returns a new enumerator that is in the same state as the current one.
old-location: winsync\ienumsyncproviderinfos_clone.htm
tech.root: winsync
ms.assetid: de53dade-82f3-418c-a44c-58d4b7502729
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],IEnumSyncProviderInfos interface, IEnumSyncProviderInfos interface [Windows Sync],Clone method, IEnumSyncProviderInfos.Clone, IEnumSyncProviderInfos::Clone, syncregistration/IEnumSyncProviderInfos::Clone, winsync.ienumsyncproviderinfos_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: syncregistration.h
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
 - Syncregistration.h
api_name:
 - IEnumSyncProviderInfos.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- syncregistration.h
: 
- IEnumSyncProviderInfos.Clone
: 
---

# IEnumSyncProviderInfos::Clone


## -description


Clones the enumerator and returns a new enumerator that is in the same state as the current one.


## -parameters




### -param ppEnum [out]

Returns the newly cloned enumerator.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to clone the enumerator.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/58b0dcc2-861a-4138-872a-cbbe2bb2cc4d">IEnumSyncProviderInfos Interface</a>
 

 

