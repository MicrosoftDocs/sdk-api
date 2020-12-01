---
UID: NN:cscobj.IOfflineFilesConnectionInfo
title: IOfflineFilesConnectionInfo (cscobj.h)
description: Presents query and action capabilities associated with the online-offline transition behavior of Offline Files.
helpviewer_keywords: ["IOfflineFilesConnectionInfo","IOfflineFilesConnectionInfo interface [Offline Files]","IOfflineFilesConnectionInfo interface [Offline Files]","described","cscobj/IOfflineFilesConnectionInfo","of.iofflinefilesconnectioninfo"]
old-location: of\iofflinefilesconnectioninfo.htm
tech.root: of
ms.assetid: 923c5657-67e7-498a-a46b-97d44368cf3b
ms.date: 12/05/2018
ms.keywords: IOfflineFilesConnectionInfo, IOfflineFilesConnectionInfo interface [Offline Files], IOfflineFilesConnectionInfo interface [Offline Files],described, cscobj/IOfflineFilesConnectionInfo, of.iofflinefilesconnectioninfo
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
 - IOfflineFilesConnectionInfo
 - cscobj/IOfflineFilesConnectionInfo
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
 - IOfflineFilesConnectionInfo
---

# IOfflineFilesConnectionInfo interface


## -description

Presents query and action capabilities associated with the online-offline transition behavior of Offline Files.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesConnectionInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesConnectionInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesConnectionInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">GetConnectState</a>
</td>
<td align="left" width="63%">
Determines whether an item is online or offline and, if offline, why.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-setconnectstate">SetConnectState</a>
</td>
<td align="left" width="63%">
Sets the connection state for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-transitionoffline">TransitionOffline</a>
</td>
<td align="left" width="63%">
Transitions an item offline if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-transitiononline">TransitionOnline</a>
</td>
<td align="left" width="63%">
Transitions an item online if possible.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>