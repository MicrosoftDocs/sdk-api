---
UID: NN:syncregistration.ISyncProviderRegistration
title: ISyncProviderRegistration
author: windows-sdk-content
description: Represents synchronization provider registration.
old-location: winsync\isyncproviderregistration.htm
old-project: winsync
ms.assetid: e7cf0c05-9d07-4630-ae34-9a9dd81492b2
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ISyncProviderRegistration, ISyncProviderRegistration interface [Windows Sync], ISyncProviderRegistration interface [Windows Sync],described, syncregistration/ISyncProviderRegistration, winsync.isyncproviderregistration
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
tech.root: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderRegistration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration interface


## -description


Represents synchronization provider registration. This is the core registration interface that contains methods for creating, modifying, and enumerating registered synchronization providers and configuration UIs. This interface can be retrieved by calling <b>CoCreate</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProviderRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncProviderRegistration</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a61b07b3-45ce-429e-9641-4cebc5b44c1b">CreateSyncProviderConfigUIRegistrationInstance</a>
</td>
<td align="left" width="63%">
Creates an in-memory instance of a synchronization provider configuration UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/637cf465-5d43-42d3-b7b9-3bd674135038">CreateSyncProviderRegistrationInstance</a>
</td>
<td align="left" width="63%">
Creates an in-memory instance of a synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36a2b498-237e-418a-b5b8-5f9bcdfbe734">EnumerateSyncProviderConfigUIs</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/d8b4f4a4-b238-431f-a123-edebe07ea7b0">IEnumSyncProviderConfigUIInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderConfigUIInfo</b> objects for the specified  criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5028b1e7-425d-4fac-ba6b-27a0cc70b378">EnumerateSyncProviderConfigUIsForContentType</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/d8b4f4a4-b238-431f-a123-edebe07ea7b0">IEnumSyncProviderConfigUIInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderConfigUIInfo</b> objects for a specified  content type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36a2b498-237e-418a-b5b8-5f9bcdfbe734">EnumerateSyncProviders</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/58b0dcc2-861a-4138-872a-cbbe2bb2cc4d">IEnumSyncProviderInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderInfo</b> objects for the specified  criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a65ba8b-b9cb-4d8c-8d18-9627547f9982">GetChange</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/45376bd2-1f5f-4f4c-9c4c-f5add9438d5c">ISyncRegistrationChange</a> object that represents a new registration event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/472732d7-39bd-434c-80f3-9808eca9035c">GetSyncProviderConfigUIFromInstanceId</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/27757aa1-a42d-4f66-99a8-bf66385fbec1">ISyncProviderConfigUI</a> object for the particular unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/687f2f28-378e-456c-a06a-d78e486e6635">GetSyncProviderConfigUIInfo</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/b7c49533-d289-44b0-9a9e-cfa47af3a087">ISyncProviderConfigUIInfo</a> object for the particular unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ef774f8-0b97-44ee-8bb9-7adf2293cc23">GetSyncProviderConfigUIInfoforProvider</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/b7c49533-d289-44b0-9a9e-cfa47af3a087">ISyncProviderConfigUIInfo</a> object for the specified synchronization provider instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed204998-9e9a-4bac-b178-b4137be87ff4">GetSyncProviderFromInstanceId</a>
</td>
<td align="left" width="63%">
Returns an initialized and instantiated  <a href="https://msdn.microsoft.com/53970f17-2857-4624-8594-069cceb93b1e">IRegisteredSyncProvider</a> object for the specific unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/894d2314-2210-4a16-a7e6-1ee74638c035">GetSyncProviderInfo</a>
</td>
<td align="left" width="63%">
Returns an initialized and instantiated  <a href="https://msdn.microsoft.com/27757aa1-a42d-4f66-99a8-bf66385fbec1">ISyncProviderConfigUI</a> object for the particular unique instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e2e2e17-e435-4def-9aee-9109e0e06a8c">GetSyncProviderState</a>
</td>
<td align="left" width="63%">
Returns the state of the specified synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b636a3b4-2ac2-4400-b8ed-4430f598db7b">RegisterForEvent</a>
</td>
<td align="left" width="63%">
Registers the user to receive notification of the arrival of new registration
		events that occur when changes are made to the registration store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcc4901a-1507-461e-bbcc-a9e440ec05ce">RevokeEvent</a>
</td>
<td align="left" width="63%">
Unregisters the user from the notification of the arrival of new registration
		events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/441df857-0498-4c6f-b279-495f1138e9c7">SetSyncProviderState</a>
</td>
<td align="left" width="63%">
Sets the state of the specified synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5b651b2-a0a5-404f-afbe-3256bf52f25f">UnregisterSyncProvider</a>
</td>
<td align="left" width="63%">
Unregisters and removes the specified synchronization provider from the registration store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14d0ab85-afd7-4615-8606-ec403a3dd453">UnregisterSyncProviderConfigUI</a>
</td>
<td align="left" width="63%">
Unregisters and removes the specified synchronization provider configuration UI from the registration store.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8233671e-bf89-448d-8347-9b4f0ae7501f">Windows Sync Registration Reference</a>
 

 

