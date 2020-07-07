---
UID: NN:imapi.IDiscMasterProgressEvents
title: IDiscMasterProgressEvents (imapi.h)
description: The IDiscMasterProgressEvents interface provides a single interface for all callbacks that can be made from IMAPI to an application.
helpviewer_keywords: ["IDiscMasterProgressEvents","IDiscMasterProgressEvents interface [IMAPI]","IDiscMasterProgressEvents interface [IMAPI]","described","_win32_idiscmasterprogressevents","base.idiscmasterprogressevents","imapi.idiscmasterprogressevents","imapi/IDiscMasterProgressEvents"]
old-location: imapi\idiscmasterprogressevents.htm
tech.root: imapi
ms.assetid: 68f7edbd-4a06-4e8d-a562-21a65767aff6
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents, IDiscMasterProgressEvents interface [IMAPI], IDiscMasterProgressEvents interface [IMAPI],described, _win32_idiscmasterprogressevents, base.idiscmasterprogressevents, imapi.idiscmasterprogressevents, imapi/IDiscMasterProgressEvents
f1_keywords:
- imapi/IDiscMasterProgressEvents
dev_langs:
- c++
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Actxprxy.dll
api_name:
- IDiscMasterProgressEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscMasterProgressEvents interface


## -description


The 
<b>IDiscMasterProgressEvents</b> interface provides a single interface for all callbacks that can be made from IMAPI to an application. An application implements this interface on one of its objects and then registers it using 
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-progressadvise">IDiscMaster::ProgressAdvise</a>. All but one of the methods in this interface are related to progress during staging or burns. Even if an application is not interested in a particular callback, it must implement the callback function and return E_NOTIMPL on the call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscMasterProgressEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiscMasterProgressEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscMasterProgressEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifyaddprogress">NotifyAddProgress</a>
</td>
<td align="left" width="63%">
Reports progress of audio/data staging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifyblockprogress">NotifyBlockProgress</a>
</td>
<td align="left" width="63%">
Reports progress of audio/data burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifyburncomplete">NotifyBurnComplete</a>
</td>
<td align="left" width="63%">
Reports that the burn is fully complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifyclosingdisc">NotifyClosingDisc</a>
</td>
<td align="left" width="63%">
Reports progress while closing a disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifyerasecomplete">NotifyEraseComplete</a>
</td>
<td align="left" width="63%">
Reports that an erase is fully complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifypnpactivity">NotifyPnPActivity</a>
</td>
<td align="left" width="63%">
Reports possible changes to recorder list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifypreparingburn">NotifyPreparingBurn</a>
</td>
<td align="left" width="63%">
Reports progress during burn setup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifytrackprogress">NotifyTrackProgress</a>
</td>
<td align="left" width="63%">
Reports progress of an audio burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-querycancel">QueryCancel</a>
</td>
<td align="left" width="63%">
Checks whether a burn is to be canceled.

</td>
</tr>
</table> 

