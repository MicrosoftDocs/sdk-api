---
UID: NN:cscobj.IOfflineFilesPinInfo
title: IOfflineFilesPinInfo (cscobj.h)
description: Represents the pinned status of an item in the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesPinInfo","IOfflineFilesPinInfo interface [Offline Files]","IOfflineFilesPinInfo interface [Offline Files]","described","cscobj/IOfflineFilesPinInfo","of.iofflinefilespininfo"]
old-location: of\iofflinefilespininfo.htm
tech.root: of
ms.assetid: 529a529a-fbeb-4414-b4c9-46bfcca4aa7a
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo, IOfflineFilesPinInfo interface [Offline Files], IOfflineFilesPinInfo interface [Offline Files],described, cscobj/IOfflineFilesPinInfo, of.iofflinefilespininfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesPinInfo
 - cscobj/IOfflineFilesPinInfo
dev_langs:
 - c++
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
---

# IOfflineFilesPinInfo interface


## -description

Represents the pinned status of an item in the Offline Files cache.

When an item is pinned into the Offline Files cache by using the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a> method, it may be pinned for one of the following reasons:
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

The <b>IOfflineFilesPinInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesPinInfo</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
