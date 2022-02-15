---
UID: NE:uiautomationclient.CoalesceEventsOptions
title: CoalesceEventsOptions (uiautomationclient.h)
description: Contains possible values for the CoalesceEvents property, which indicates whether an accessible technology client receives all events, or a subset where duplicate events are detected and filtered.
helpviewer_keywords: ["CoalesceEventsOptions","CoalesceEventsOptions enumeration [Windows Accessibility]","CoalesceEventsOptions_Disabled","CoalesceEventsOptions_Enabled","uiautomationclient/CoalesceEventsOptions","uiautomationclient/CoalesceEventsOptions_Disabled","uiautomationclient/CoalesceEventsOptions_Enabled","winauto.uiauto_coalesceeventsoptions_enum"]
old-location: winauto\uiauto_coalesceeventsoptions_enum.htm
tech.root: WinAuto
ms.assetid: 2CE5A02A-40B4-43BE-863E-08AD9B2A9F75
ms.date: 12/05/2018
ms.keywords: CoalesceEventsOptions, CoalesceEventsOptions enumeration [Windows Accessibility], CoalesceEventsOptions_Disabled, CoalesceEventsOptions_Enabled, uiautomationclient/CoalesceEventsOptions, uiautomationclient/CoalesceEventsOptions_Disabled, uiautomationclient/CoalesceEventsOptions_Enabled, winauto.uiauto_coalesceeventsoptions_enum
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoalesceEventsOptions
 - uiautomationclient/CoalesceEventsOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationClient.h
api_name:
 - CoalesceEventsOptions
---

# CoalesceEventsOptions enumeration


## -description

Contains possible values for the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-get_coalesceevents">CoalesceEvents</a> property, which indicates whether an accessible technology client receives all events, or a subset where duplicate events are detected and filtered.

## -enum-fields

### -field CoalesceEventsOptions_Disabled:0

Event coalescing is disabled.

### -field CoalesceEventsOptions_Enabled:0x1

Event coalescing is enabled.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-get_coalesceevents">CoalesceEvents</a>
