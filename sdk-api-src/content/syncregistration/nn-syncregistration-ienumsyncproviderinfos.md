---
UID: NN:syncregistration.IEnumSyncProviderInfos
title: IEnumSyncProviderInfos (syncregistration.h)
description: Enumerates ISyncProviderInfo objects that contain the information used to create an instance of a synchronization provider.
old-location: winsync\ienumsyncproviderinfos.htm
tech.root: winsync
ms.assetid: 58b0dcc2-861a-4138-872a-cbbe2bb2cc4d
ms.date: 12/05/2018
ms.keywords: IEnumSyncProviderInfos, IEnumSyncProviderInfos interface [Windows Sync], IEnumSyncProviderInfos interface [Windows Sync],described, syncregistration/IEnumSyncProviderInfos, winsync.ienumsyncproviderinfos
f1_keywords:
- syncregistration/IEnumSyncProviderInfos
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
- IEnumSyncProviderInfos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSyncProviderInfos interface


## -description


Enumerates <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderInfo</a> objects that contain the information used to create an instance of a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncProviderInfos</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncProviderInfos</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSyncProviderInfos</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderinfos-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderinfos-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next <b>ISyncProviderInfo</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderinfos-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the <b>ISyncProviderInfo</b> set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderinfos-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of <b>ISyncProviderInfo</b> objects.

</td>
</tr>
</table> 


## -remarks



This interface is obtained from the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-enumeratesyncproviders">ISyncProviderRegistration::EnumerateSyncProviders</a> method. The method will return an  <b>IEnumSyncProviderInfos</b> enumerator for all registered <b>ISyncProviderInfo</b> objects or for just the registered <b>ISyncProviderInfo</b> objects that match the particular filter criteria.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
 

 

