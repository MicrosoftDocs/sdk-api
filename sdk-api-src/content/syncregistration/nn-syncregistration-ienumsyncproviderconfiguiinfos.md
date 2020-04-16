---
UID: NN:syncregistration.IEnumSyncProviderConfigUIInfos
title: IEnumSyncProviderConfigUIInfos (syncregistration.h)
description: Enumerates ISyncProviderConfigUIInfo objects that contain configuration UI information used to build and register a synchronization provider.helpviewer_keywords: ["IEnumSyncProviderConfigUIInfos","IEnumSyncProviderConfigUIInfos interface [Windows Sync]","IEnumSyncProviderConfigUIInfos interface [Windows Sync]","described","syncregistration/IEnumSyncProviderConfigUIInfos","winsync.ienumsyncproviderconfiguiinfos"]
old-location: winsync\ienumsyncproviderconfiguiinfos.htm
tech.root: winsync
ms.assetid: d8b4f4a4-b238-431f-a123-edebe07ea7b0
ms.date: 12/05/2018
ms.keywords: IEnumSyncProviderConfigUIInfos, IEnumSyncProviderConfigUIInfos interface [Windows Sync], IEnumSyncProviderConfigUIInfos interface [Windows Sync],described, syncregistration/IEnumSyncProviderConfigUIInfos, winsync.ienumsyncproviderconfiguiinfos
f1_keywords:
- syncregistration/IEnumSyncProviderConfigUIInfos
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSyncProviderConfigUIInfos interface


## -description


Enumerates <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> objects that contain configuration UI information used to build and register a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncProviderConfigUIInfos</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncProviderConfigUIInfos</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderconfiguiinfos-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderconfiguiinfos-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next <b>ISyncProviderConfigUIInfo</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderconfiguiinfos-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the collection of <b>ISyncProviderConfigUIInfo</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderconfiguiinfos-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of <b>ISyncProviderConfigUIInfo</b> objects.

</td>
</tr>
</table> 


## -remarks



This interface is obtained from the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317197(v=vs.85)">ISyncProviderRegistration::EnumerateSyncProviderConfigUIsForContentType</a> method. The method will return an  <b>IEnumSyncProviderConfigUIInfos</b> enumerator for all registered <b>ISyncProviderConfigUI</b> objects or for just the registered <b>ISyncProviderConfigUI</b> objects of a particular content type.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
 

 

