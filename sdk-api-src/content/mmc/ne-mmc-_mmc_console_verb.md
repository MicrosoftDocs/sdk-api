---
UID: NE:mmc._MMC_CONSOLE_VERB
title: "_MMC_CONSOLE_VERB"
author: windows-sdk-content
description: The MMC_CONSOLE_VERB enumeration defines the command identifiers available for MMC verbs. These values are used in the m_eCmdID parameter of IConsoleVerb::GetVerbState, IConsoleVerb::SetVerbState, and IConsoleVerb::SetDefaultVerb.
old-location: mmc\mmc_console_verb.htm
old-project: MMC
ms.assetid: 153d89f4-03de-429a-9f52-36a5f6a9762f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: MMC_CONSOLE_VERB, MMC_CONSOLE_VERB enumeration [MMC], MMC_VERB_COPY, MMC_VERB_CUT, MMC_VERB_DELETE, MMC_VERB_NONE, MMC_VERB_OPEN, MMC_VERB_PASTE, MMC_VERB_PRINT, MMC_VERB_PROPERTIES, MMC_VERB_REFRESH, MMC_VERB_RENAME, _MMC_CONSOLE_VERB, _slate_mmc_console_verb, mmc.mmc_console_verb, mmc/MMC_CONSOLE_VERB, mmc/MMC_VERB_COPY, mmc/MMC_VERB_CUT, mmc/MMC_VERB_DELETE, mmc/MMC_VERB_NONE, mmc/MMC_VERB_OPEN, mmc/MMC_VERB_PASTE, mmc/MMC_VERB_PRINT, mmc/MMC_VERB_PROPERTIES, mmc/MMC_VERB_REFRESH, mmc/MMC_VERB_RENAME
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mmc.h
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
tech.root: 
req.typenames: MMC_CONSOLE_VERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_CONSOLE_VERB
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_CONSOLE_VERB enumeration


## -description


The 
<b>MMC_CONSOLE_VERB</b> enumeration defines the command identifiers available for MMC verbs. These values are used in the <i>m_eCmdID</i> parameter of 
<a href="https://msdn.microsoft.com/86388a22-5156-45e9-a601-33b7c5ca15f3">IConsoleVerb::GetVerbState</a>, 
<a href="https://msdn.microsoft.com/55cf5f73-a113-430e-be16-d7a88abe15b6">IConsoleVerb::SetVerbState</a>, and 
<a href="https://msdn.microsoft.com/099a5cd7-b1c8-45c0-a109-7e78d1b6ee98">IConsoleVerb::SetDefaultVerb</a>.


## -enum-fields




### -field MMC_VERB_NONE

No verbs specified. Snap-ins can use this verb in calls to 
<a href="https://msdn.microsoft.com/099a5cd7-b1c8-45c0-a109-7e78d1b6ee98">IConsoleVerb::SetDefaultVerb</a> to specify that the selected item does not have a default verb.


### -field MMC_VERB_OPEN

Allows the selected item to be opened.


### -field MMC_VERB_COPY

Allows the selected item to be copied to the clipboard. When the user activates this verb, MMC calls the snap-in's <a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">IComponentData::QueryDataObject</a> or <a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">IComponent::QueryDataObject</a> implementation to request a data object for the selected item.


### -field MMC_VERB_PASTE

Allows the selected item that has been cut or copied to be pasted into the result pane. When the user activates this verb, MMC sends the snap-in's <a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> method a <a href="https://msdn.microsoft.com/19259852-be87-40f6-8475-26f7cc232db6">MMCN_QUERY_PASTE</a> notification message.


### -field MMC_VERB_DELETE

Allows the selected item to be deleted. When the user activates this verb, MMC sends the snap-in's <a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> method a <a href="https://msdn.microsoft.com/eaf6c7de-2b02-4563-9392-588a74c9d744">MMCN_DELETE</a> notification message.


### -field MMC_VERB_PROPERTIES

The console instructs the snap-in and all snap-in extensions to provide property pages for the currently selected item. When the user activates this verb, MMC calls the <a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a> method of all snap-ins (primary and extension) that add property pages for the selected item.

Be aware that primary snap-ins are responsible for enabling the <b>MMC_VERB_PROPERTIES</b> verb. Extensions snap-ins cannot do this, because they do not own the item for which the verb is enabled.


### -field MMC_VERB_RENAME

Allows the selected item to be renamed. When the user activates this verb, MMC sends the snap-in's <a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> or <a href="https://msdn.microsoft.com/8679396e-23d0-4418-987a-c72b1508e7b9">IComponentData::Notify</a> method a <a href="https://msdn.microsoft.com/1a77e563-e469-466e-b61a-e127dfb19c1a">MMCN_RENAME</a> notification message.


### -field MMC_VERB_REFRESH

Determines whether the currently selected scope item (folder) can be refreshed. When the user activates this verb, MMC sends the snap-in's <a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> a <a href="https://msdn.microsoft.com/c39d99f7-7e80-4bad-8494-41f7f28c83a3">MMCN_REFRESH</a> notification message.


### -field MMC_VERB_PRINT

Determines whether the currently selected item can be printed. When the user activates this verb, MMC sends the snap-in's <a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> a <a href="https://msdn.microsoft.com/74814817-f93b-476f-a477-e6b65ed229bb">MMCN_PRINT</a> notification message.


### -field MMC_VERB_CUT

(Applies to MMC 1.1 and later.) Used only to explicitly disable or hide the cut verb, when the copy and paste verbs are enabled. When the user activates this verb, MMC calls the snap-in's <a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">IComponentData::QueryDataObject</a> or <a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">IComponent::QueryDataObject</a> implementation to request a data object for the cut item.


### -field MMC_VERB_MAX


### -field MMC_VERB_FIRST


### -field MMC_VERB_LAST



