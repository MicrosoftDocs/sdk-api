---
UID: NN:syncregistration.ISyncProviderConfigUI
title: ISyncProviderConfigUI (syncregistration.h)
description: Represents configuration UI information used to build and register a synchronization provider.helpviewer_keywords: ["ISyncProviderConfigUI","ISyncProviderConfigUI interface [Windows Sync]","ISyncProviderConfigUI interface [Windows Sync]","described","syncregistration/ISyncProviderConfigUI","winsync.isyncproviderconfigui"]
old-location: winsync\isyncproviderconfigui.htm
tech.root: winsync
ms.assetid: 27757aa1-a42d-4f66-99a8-bf66385fbec1
ms.date: 12/05/2018
ms.keywords: ISyncProviderConfigUI, ISyncProviderConfigUI interface [Windows Sync], ISyncProviderConfigUI interface [Windows Sync],described, syncregistration/ISyncProviderConfigUI, winsync.isyncproviderconfigui
f1_keywords:
- syncregistration/ISyncProviderConfigUI
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
- ISyncProviderConfigUI
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncProviderConfigUI interface


## -description


Represents configuration UI information used to build and register a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProviderConfigUI</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncProviderConfigUI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncProviderConfigUI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderconfigui-createandregisternewsyncprovider">CreateAndRegisterNewSyncProvider</a>
</td>
<td align="left" width="63%">
Creates and registers a new  synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderconfigui-getregisteredproperties">GetRegisteredProperties</a>
</td>
<td align="left" width="63%">
Obtains configuration UI properties for reading and writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderconfigui-init">Init</a>
</td>
<td align="left" width="63%">
Initializes the configuration UI for a synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderconfigui-modifysyncprovider">ModifySyncProvider</a>
</td>
<td align="left" width="63%">
Updates the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> of the synchronization provider that is configured by this <b>ISyncProviderConfigUI</b>.

</td>
</tr>
</table> 


## -remarks



The writer of a synchronization provider should implement an <b>ISyncProviderConfigUI</b> (a builder) for a synchronization provider if it requires additional information and properties to be set before it can be created. For example, a synchronization provider may require a user to enter credentials before their data can be synchronized.

If the registered synchronization provider is a <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a> provider, then the <b>Init</b>method will be called by the Sync Framework synchronization session. For more information about the different types of synchronization providers you can write for Windows, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
 

 

