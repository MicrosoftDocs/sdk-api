---
UID: NN:cscobj.IOfflineFilesPinInfo
title: IOfflineFilesPinInfo (cscobj.h)
author: windows-sdk-content
description: Represents the pinned status of an item in the Offline Files cache.
old-location: of\iofflinefilespininfo.htm
tech.root: offlinefiles
ms.assetid: 529a529a-fbeb-4414-b4c9-46bfcca4aa7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo, IOfflineFilesPinInfo interface [Offline Files], IOfflineFilesPinInfo interface [Offline Files],described, cscobj/IOfflineFilesPinInfo, of.iofflinefilespininfo
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesPinInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesPinInfo interface


## -description


Represents the pinned status of an item in the Offline Files cache.

When an item is pinned into the Offline Files cache by using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a> method, it may be pinned for one of the following reasons:
<table>
<tr>
<th>Flag Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER</b></td>
<td>This flag is set when a file is pinned using the "Always available offline" option in Windows explorer.</td>
</tr>
<tr>
<td><b>OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER_POLICY</b></td>
<td>This flag is set when a file is pinned by the per-user "Administratively assigned offline files" Group Policy.</td>
</tr>
<tr>
<td><b>OFFLINEFILES_PIN_CONTROL_FLAG_FORALL</b></td>
<td>This flag is set when a file is pinned by the per-computer "Administratively assigned offline files" Group Policy.</td>
</tr>
<tr>
<td><b>OFFLINEFILES_PIN_CONTROL_FLAG_FORREDIR</b></td>
<td>This flag is set when a redirected folder is pinned by Folder Redirection.</td>
</tr>
</table> 

Each of the various <i>IsPinnedForUserXxxxxx</i> methods expresses one of these reasons.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesPinInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesPinInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesPinInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilespininfo-ispinned">IsPinned</a>
</td>
<td align="left" width="63%">
Determines whether the item is pinned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilespininfo-ispinnedforcomputer">IsPinnedForComputer</a>
</td>
<td align="left" width="63%">
Determines whether the item was pinned for all users on the computer by Group Policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilespininfo-ispinnedforfolderredirection">IsPinnedForFolderRedirection</a>
</td>
<td align="left" width="63%">
Determines whether the item was pinned by Folder Redirection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilespininfo-ispinnedforuser">IsPinnedForUser</a>
</td>
<td align="left" width="63%">
Determines whether the item was pinned by a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilespininfo-ispinnedforuserbypolicy">IsPinnedForUserByPolicy</a>
</td>
<td align="left" width="63%">
Determines whether the item was pinned for users by Group Policy.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

