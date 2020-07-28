---
UID: NN:syncregistration.ISyncProviderRegistration
title: ISyncProviderRegistration (syncregistration.h)
description: Represents synchronization provider registration.
helpviewer_keywords: ["ISyncProviderRegistration","ISyncProviderRegistration interface [Windows Sync]","ISyncProviderRegistration interface [Windows Sync]","described","syncregistration/ISyncProviderRegistration","winsync.isyncproviderregistration"]
old-location: winsync\isyncproviderregistration.htm
tech.root: winsync
ms.assetid: e7cf0c05-9d07-4630-ae34-9a9dd81492b2
ms.date: 12/05/2018
ms.keywords: ISyncProviderRegistration, ISyncProviderRegistration interface [Windows Sync], ISyncProviderRegistration interface [Windows Sync],described, syncregistration/ISyncProviderRegistration, winsync.isyncproviderregistration
f1_keywords:
- syncregistration/ISyncProviderRegistration
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
- ISyncProviderRegistration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncProviderRegistration interface


## -description


Represents synchronization provider registration. This is the core registration interface that contains methods for creating, modifying, and enumerating registered synchronization providers and configuration UIs. This interface can be retrieved by calling <b>CoCreate</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProviderRegistration</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncProviderRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncProviderRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-createsyncproviderconfiguiregistrationinstance">CreateSyncProviderConfigUIRegistrationInstance</a>
</td>
<td align="left" width="63%">
Creates an in-memory instance of a synchronization provider configuration UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-createsyncproviderregistrationinstance">CreateSyncProviderRegistrationInstance</a>
</td>
<td align="left" width="63%">
Creates an in-memory instance of a synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-enumeratesyncproviders">EnumerateSyncProviderConfigUIs</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderconfiguiinfos">IEnumSyncProviderConfigUIInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderConfigUIInfo</b> objects for the specified  criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317197(v=vs.85)">EnumerateSyncProviderConfigUIsForContentType</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderconfiguiinfos">IEnumSyncProviderConfigUIInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderConfigUIInfo</b> objects for a specified  content type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-enumeratesyncproviders">EnumerateSyncProviders</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderinfos">IEnumSyncProviderInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderInfo</b> objects for the specified  criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getchange">GetChange</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncregistrationchange">ISyncRegistrationChange</a> object that represents a new registration event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguifrominstanceid">GetSyncProviderConfigUIFromInstanceId</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI</a> object for the particular unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguiinfo">GetSyncProviderConfigUIInfo</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> object for the particular unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguiinfoforprovider">GetSyncProviderConfigUIInfoforProvider</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> object for the specified synchronization provider instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderfrominstanceid">GetSyncProviderFromInstanceId</a>
</td>
<td align="left" width="63%">
Returns an initialized and instantiated  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-iregisteredsyncprovider">IRegisteredSyncProvider</a> object for the specific unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderinfo">GetSyncProviderInfo</a>
</td>
<td align="left" width="63%">
Returns an initialized and instantiated  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI</a> object for the particular unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderstate">GetSyncProviderState</a>
</td>
<td align="left" width="63%">
Returns the state of the specified synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-registerforevent">RegisterForEvent</a>
</td>
<td align="left" width="63%">
Registers the user to receive notification of the arrival of new registration
		events that occur when changes are made to the registration store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-revokeevent">RevokeEvent</a>
</td>
<td align="left" width="63%">
Unregisters the user from the notification of the arrival of new registration
		events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-setsyncproviderstate">SetSyncProviderState</a>
</td>
<td align="left" width="63%">
Sets the state of the specified synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-unregistersyncprovider">UnregisterSyncProvider</a>
</td>
<td align="left" width="63%">
Unregisters and removes the specified synchronization provider from the registration store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-unregistersyncproviderconfigui">UnregisterSyncProviderConfigUI</a>
</td>
<td align="left" width="63%">
Unregisters and removes the specified synchronization provider configuration UI from the registration store.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
 

 

