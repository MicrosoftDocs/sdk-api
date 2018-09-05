---
UID: NF:syncregistration.IEnumSyncProviderConfigUIInfos.Next
title: IEnumSyncProviderConfigUIInfos::Next
author: windows-sdk-content
description: Returns the next ISyncProviderConfigUIInfo object.
old-location: winsync\ienumsyncproviderconfiguiinfos_next.htm
old-project: winsync
ms.assetid: 46564ed2-233d-409c-a996-dd3d9cfde907
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumSyncProviderConfigUIInfos interface [Windows Sync],Next method, IEnumSyncProviderConfigUIInfos.Next, IEnumSyncProviderConfigUIInfos::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumSyncProviderConfigUIInfos interface, syncregistration/IEnumSyncProviderConfigUIInfos::Next, winsync.ienumsyncproviderconfiguiinfos_next
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
 - IEnumSyncProviderConfigUIInfos.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumSyncProviderConfigUIInfos::Next


## -description


Returns the next <b>ISyncProviderConfigUIInfo</b> object.


## -parameters




### -param cFactories [in]

The number of <b>ISyncProviderConfigUIInfo</b> objects to retrieve in the range of zero to 1.


### -param ppSyncProviderConfigUIInfo [out]

Returns the next <i>pcFetched</i><b>ISyncProviderConfigUIInfo</b> objects.


### -param pcFetched [out]

Returns the number of <b>ISyncProviderConfigUIInfo</b> objects that are retrieved.


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
The requested number of objects was not available.

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
There was not enough memory available to return the next  <b>ISyncProviderConfigUIInfo</b> object.

</td>
</tr>
</table>
 




## -remarks



This method will attempt to return the number of items specified by the <i>cFactories</i> parameter.  If the specified number of items is not available, <b>S_FALSE</b> will be returned, and <i>pcFetched</i> will contain the number of items that were able to be retrieved.




## -see-also




<a href="https://msdn.microsoft.com/d8b4f4a4-b238-431f-a123-edebe07ea7b0">IEnumSyncProviderConfigUIInfos Interface</a>
 

 

