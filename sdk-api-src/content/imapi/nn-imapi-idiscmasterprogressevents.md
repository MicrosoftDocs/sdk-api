---
UID: NN:imapi.IDiscMasterProgressEvents
title: IDiscMasterProgressEvents
author: windows-sdk-content
description: The IDiscMasterProgressEvents interface provides a single interface for all callbacks that can be made from IMAPI to an application.
old-location: imapi\idiscmasterprogressevents.htm
tech.root: imapi
ms.assetid: 68f7edbd-4a06-4e8d-a562-21a65767aff6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IDiscMasterProgressEvents, IDiscMasterProgressEvents interface [IMAPI], IDiscMasterProgressEvents interface [IMAPI],described, _win32_idiscmasterprogressevents, base.idiscmasterprogressevents, imapi.idiscmasterprogressevents, imapi/IDiscMasterProgressEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscMasterProgressEvents interface


## -description


The 
<b>IDiscMasterProgressEvents</b> interface provides a single interface for all callbacks that can be made from IMAPI to an application. An application implements this interface on one of its objects and then registers it using 
<a href="https://msdn.microsoft.com/64966230-2042-46cb-9974-adbe382723a1">IDiscMaster::ProgressAdvise</a>. All but one of the methods in this interface are related to progress during staging or burns. Even if an application is not interested in a particular callback, it must implement the callback function and return E_NOTIMPL on the call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscMasterProgressEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDiscMasterProgressEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d367b789-430e-48f5-9e50-5d6ffb9d7ebc">NotifyAddProgress</a>
</td>
<td align="left" width="63%">
Reports progress of audio/data staging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c156be7-5ba4-48e7-a0d1-b0b8d69b30e2">NotifyBlockProgress</a>
</td>
<td align="left" width="63%">
Reports progress of audio/data burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/deefe7cb-60aa-4255-a7b1-261fb40e6318">NotifyBurnComplete</a>
</td>
<td align="left" width="63%">
Reports that the burn is fully complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eeccb4e-0e49-40a9-b659-f0784f921074">NotifyClosingDisc</a>
</td>
<td align="left" width="63%">
Reports progress while closing a disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17a0debe-919d-4db7-bcbb-eb4fc9973d83">NotifyEraseComplete</a>
</td>
<td align="left" width="63%">
Reports that an erase is fully complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2b41e86-2f1b-46f1-955d-7fc42f8189a4">NotifyPnPActivity</a>
</td>
<td align="left" width="63%">
Reports possible changes to recorder list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28aced4e-6e7e-40fe-a00a-c0e470815cac">NotifyPreparingBurn</a>
</td>
<td align="left" width="63%">
Reports progress during burn setup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb1eafe9-d907-4b41-8e4d-03f1b3f51012">NotifyTrackProgress</a>
</td>
<td align="left" width="63%">
Reports progress of an audio burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca7ad8cb-0792-41ec-be5b-147be6750442">QueryCancel</a>
</td>
<td align="left" width="63%">
Checks whether a burn is to be canceled.

</td>
</tr>
</table> 

