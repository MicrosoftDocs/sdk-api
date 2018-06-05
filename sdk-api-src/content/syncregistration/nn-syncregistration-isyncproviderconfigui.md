---
UID: NN:syncregistration.ISyncProviderConfigUI
title: ISyncProviderConfigUI
author: windows-sdk-content
description: Represents configuration UI information used to build and register a synchronization provider.
old-location: winsync\isyncproviderconfigui.htm
old-project: winsync
ms.assetid: 27757aa1-a42d-4f66-99a8-bf66385fbec1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncProviderConfigUI, ISyncProviderConfigUI interface [Windows Sync], ISyncProviderConfigUI interface [Windows Sync],described, syncregistration/ISyncProviderConfigUI, winsync.isyncproviderconfigui
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncregistration.h
api_name:
-	ISyncProviderConfigUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderConfigUI interface


## -description


Represents configuration UI information used to build and register a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProviderConfigUI</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncProviderConfigUI</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4b256431-ed9a-414d-88c2-89f02000410d">CreateAndRegisterNewSyncProvider</a>
</td>
<td align="left" width="63%">
Creates and registers a new  synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c96091d7-4b80-445b-911a-fde612eafce9">GetRegisteredProperties</a>
</td>
<td align="left" width="63%">
Obtains configuration UI properties for reading and writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes the configuration UI for a synchronization provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16f6d30c-422a-4638-a63b-f9d2a5fdb8b4">ModifySyncProvider</a>
</td>
<td align="left" width="63%">
Updates the <a href="https://msdn.microsoft.com/fe50e34c-6499-4c1e-b891-7b4f797510f2">ISyncProviderInfo</a> of the synchronization provider that is configured by this <b>ISyncProviderConfigUI</b>.

</td>
</tr>
</table> 


## -remarks



The writer of a synchronization provider should implement an <b>ISyncProviderConfigUI</b> (a builder) for a synchronization provider if it requires additional information and properties to be set before it can be created. For example, a synchronization provider may require a user to enter credentials before their data can be synchronized.

If the registered synchronization provider is a <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a> provider, then the <b>Init</b>

method will be called by the Sync Framework synchronization session. For more information about the different types of synchronization providers you can write for Windows, see <a href="https://msdn.microsoft.com/acf9a557-da4f-4688-9fea-9456947c17b4">Options for Building a Synchronization Provider</a>.




## -see-also




<a href="https://msdn.microsoft.com/8233671e-bf89-448d-8347-9b4f0ae7501f">Windows Sync Registration Reference</a>
 

 

