---
UID: NE:mmc._MMC_CONSOLE_VERB
title: MMC_CONSOLE_VERB (mmc.h)
description: The MMC_CONSOLE_VERB enumeration defines the command identifiers available for MMC verbs. These values are used in the m_eCmdID parameter of IConsoleVerb::GetVerbState, IConsoleVerb::SetVerbState, and IConsoleVerb::SetDefaultVerb.
helpviewer_keywords: ["MMC_CONSOLE_VERB","MMC_CONSOLE_VERB enumeration [MMC]","MMC_VERB_COPY","MMC_VERB_CUT","MMC_VERB_DELETE","MMC_VERB_NONE","MMC_VERB_OPEN","MMC_VERB_PASTE","MMC_VERB_PRINT","MMC_VERB_PROPERTIES","MMC_VERB_REFRESH","MMC_VERB_RENAME","_slate_mmc_console_verb","mmc.mmc_console_verb","mmc/MMC_CONSOLE_VERB","mmc/MMC_VERB_COPY","mmc/MMC_VERB_CUT","mmc/MMC_VERB_DELETE","mmc/MMC_VERB_NONE","mmc/MMC_VERB_OPEN","mmc/MMC_VERB_PASTE","mmc/MMC_VERB_PRINT","mmc/MMC_VERB_PROPERTIES","mmc/MMC_VERB_REFRESH","mmc/MMC_VERB_RENAME"]
old-location: mmc\mmc_console_verb.htm
tech.root: mmc
ms.assetid: 153d89f4-03de-429a-9f52-36a5f6a9762f
ms.date: 12/05/2018
ms.keywords: MMC_CONSOLE_VERB, MMC_CONSOLE_VERB enumeration [MMC], MMC_VERB_COPY, MMC_VERB_CUT, MMC_VERB_DELETE, MMC_VERB_NONE, MMC_VERB_OPEN, MMC_VERB_PASTE, MMC_VERB_PRINT, MMC_VERB_PROPERTIES, MMC_VERB_REFRESH, MMC_VERB_RENAME, _slate_mmc_console_verb, mmc.mmc_console_verb, mmc/MMC_CONSOLE_VERB, mmc/MMC_VERB_COPY, mmc/MMC_VERB_CUT, mmc/MMC_VERB_DELETE, mmc/MMC_VERB_NONE, mmc/MMC_VERB_OPEN, mmc/MMC_VERB_PASTE, mmc/MMC_VERB_PRINT, mmc/MMC_VERB_PROPERTIES, mmc/MMC_VERB_REFRESH, mmc/MMC_VERB_RENAME
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MMC_CONSOLE_VERB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_CONSOLE_VERB
 - mmc/_MMC_CONSOLE_VERB
 - MMC_CONSOLE_VERB
 - mmc/MMC_CONSOLE_VERB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_CONSOLE_VERB
---

# MMC_CONSOLE_VERB enumeration


## -description

The 
<b>MMC_CONSOLE_VERB</b> enumeration defines the command identifiers available for MMC verbs. These values are used in the <i>m_eCmdID</i> parameter of 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsoleverb-getverbstate">IConsoleVerb::GetVerbState</a>, 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsoleverb-setverbstate">IConsoleVerb::SetVerbState</a>, and 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsoleverb-setdefaultverb">IConsoleVerb::SetDefaultVerb</a>.

## -enum-fields

### -field MMC_VERB_NONE:0x0000

No verbs specified. Snap-ins can use this verb in calls to 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsoleverb-setdefaultverb">IConsoleVerb::SetDefaultVerb</a> to specify that the selected item does not have a default verb.

### -field MMC_VERB_OPEN:0x8000

Allows the selected item to be opened.

### -field MMC_VERB_COPY:0x8001

Allows the selected item to be copied to the clipboard. When the user activates this verb, MMC calls the snap-in's <a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">IComponentData::QueryDataObject</a> or <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a> implementation to request a data object for the selected item.

### -field MMC_VERB_PASTE:0x8002

Allows the selected item that has been cut or copied to be pasted into the result pane. When the user activates this verb, MMC sends the snap-in's <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> method a <a href="/previous-versions/windows/desktop/mmc/mmcn-query-paste">MMCN_QUERY_PASTE</a> notification message.

### -field MMC_VERB_DELETE:0x8003

Allows the selected item to be deleted. When the user activates this verb, MMC sends the snap-in's <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> method a <a href="/previous-versions/windows/desktop/mmc/mmcn-delete">MMCN_DELETE</a> notification message.

### -field MMC_VERB_PROPERTIES:0x8004

The console instructs the snap-in and all snap-in extensions to provide property pages for the currently selected item. When the user activates this verb, MMC calls the <a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a> method of all snap-ins (primary and extension) that add property pages for the selected item.

Be aware that primary snap-ins are responsible for enabling the <b>MMC_VERB_PROPERTIES</b> verb. Extensions snap-ins cannot do this, because they do not own the item for which the verb is enabled.

### -field MMC_VERB_RENAME:0x8005

Allows the selected item to be renamed. When the user activates this verb, MMC sends the snap-in's <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> or <a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify">IComponentData::Notify</a> method a <a href="/previous-versions/windows/desktop/mmc/mmcn-rename">MMCN_RENAME</a> notification message.

### -field MMC_VERB_REFRESH:0x8006

Determines whether the currently selected scope item (folder) can be refreshed. When the user activates this verb, MMC sends the snap-in's <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> a <a href="/previous-versions/windows/desktop/mmc/mmcn-refresh">MMCN_REFRESH</a> notification message.

### -field MMC_VERB_PRINT:0x8007

Determines whether the currently selected item can be printed. When the user activates this verb, MMC sends the snap-in's <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> a <a href="/previous-versions/windows/desktop/mmc/mmcn-print">MMCN_PRINT</a> notification message.

### -field MMC_VERB_CUT:0x8008

(Applies to MMC 1.1 and later.) Used only to explicitly disable or hide the cut verb, when the copy and paste verbs are enabled. When the user activates this verb, MMC calls the snap-in's <a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">IComponentData::QueryDataObject</a> or <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a> implementation to request a data object for the cut item.

### -field MMC_VERB_MAX

### -field MMC_VERB_FIRST

### -field MMC_VERB_LAST
