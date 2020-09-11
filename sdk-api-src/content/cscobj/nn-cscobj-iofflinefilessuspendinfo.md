---
UID: NN:cscobj.IOfflineFilesSuspendInfo
title: IOfflineFilesSuspendInfo (cscobj.h)
description: Determines whether an item is suspended or not and, if so, if it is a suspended root or not.
helpviewer_keywords: ["IOfflineFilesSuspendInfo","IOfflineFilesSuspendInfo interface [Offline Files]","IOfflineFilesSuspendInfo interface [Offline Files]","described","cscobj/IOfflineFilesSuspendInfo","of.iofflinefilessuspendinfo"]
old-location: of\iofflinefilessuspendinfo.htm
tech.root: of
ms.assetid: b9f9e30e-df37-467e-ac59-7955e0eae3c0
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSuspendInfo, IOfflineFilesSuspendInfo interface [Offline Files], IOfflineFilesSuspendInfo interface [Offline Files],described, cscobj/IOfflineFilesSuspendInfo, of.iofflinefilessuspendinfo
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
 - IOfflineFilesSuspendInfo
 - cscobj/IOfflineFilesSuspendInfo
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
 - IOfflineFilesSuspendInfo
---

# IOfflineFilesSuspendInfo interface


## -description

Determines whether an item is suspended or not and, if so, if it is a suspended root or not.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSuspendInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesSuspendInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSuspendInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessuspendinfo-issuspended">IsSuspended</a>
</td>
<td align="left" width="63%">
Determines whether an item is suspended.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>

