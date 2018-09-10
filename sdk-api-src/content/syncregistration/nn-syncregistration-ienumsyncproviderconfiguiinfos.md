---
UID: NN:syncregistration.IEnumSyncProviderConfigUIInfos
title: IEnumSyncProviderConfigUIInfos
author: windows-sdk-content
description: Enumerates ISyncProviderConfigUIInfo objects that contain configuration UI information used to build and register a synchronization provider.
old-location: winsync\ienumsyncproviderconfiguiinfos.htm
tech.root: winsync
ms.assetid: d8b4f4a4-b238-431f-a123-edebe07ea7b0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumSyncProviderConfigUIInfos, IEnumSyncProviderConfigUIInfos interface [Windows Sync], IEnumSyncProviderConfigUIInfos interface [Windows Sync],described, syncregistration/IEnumSyncProviderConfigUIInfos, winsync.ienumsyncproviderconfiguiinfos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IEnumSyncProviderConfigUIInfos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSyncProviderConfigUIInfos interface


## -description


Enumerates <a href="https://msdn.microsoft.com/b7c49533-d289-44b0-9a9e-cfa47af3a087">ISyncProviderConfigUIInfo</a> objects that contain configuration UI information used to build and register a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncProviderConfigUIInfos</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSyncProviderConfigUIInfos</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSyncProviderConfigUIInfos</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30f2a85a-86c2-4547-a18f-448a01d64d9b">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46564ed2-233d-409c-a996-dd3d9cfde907">Next</a>
</td>
<td align="left" width="63%">
Returns the next <b>ISyncProviderConfigUIInfo</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae976a03-c0e3-4a47-8153-8ba947ac8ea0">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the collection of <b>ISyncProviderConfigUIInfo</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ecd6cce-77af-423a-9b95-80b1d7ec9d2f">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of <b>ISyncProviderConfigUIInfo</b> objects.

</td>
</tr>
</table> 


## -remarks



This interface is obtained from the  <a href="https://msdn.microsoft.com/5028b1e7-425d-4fac-ba6b-27a0cc70b378">ISyncProviderRegistration::EnumerateSyncProviderConfigUIsForContentType</a> method. The method will return an  <b>IEnumSyncProviderConfigUIInfos</b> enumerator for all registered <b>ISyncProviderConfigUI</b> objects or for just the registered <b>ISyncProviderConfigUI</b> objects of a particular content type.




## -see-also




<a href="https://msdn.microsoft.com/8233671e-bf89-448d-8347-9b4f0ae7501f">Windows Sync Registration Reference</a>
 

 

