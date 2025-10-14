---
UID: NS:fwpmtypes.FWPM_VSWITCH_EVENT0_
title: FWPM_VSWITCH_EVENT0 (fwpmtypes.h)
description: Contains information about a vSwitch event.
helpviewer_keywords: ["FWPM_VSWITCH_EVENT0","FWPM_VSWITCH_EVENT0 structure [Filtering]","fwp.fwpm_vswitch_event0","fwpmtypes/FWPM_VSWITCH_EVENT0"]
old-location: fwp\fwpm_vswitch_event0.htm
tech.root: fwp
ms.assetid: bd25f66a-511a-470d-a33a-5e73d8b802c2
ms.date: 12/05/2018
ms.keywords: FWPM_VSWITCH_EVENT0, FWPM_VSWITCH_EVENT0 structure [Filtering], fwp.fwpm_vswitch_event0, fwpmtypes/FWPM_VSWITCH_EVENT0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_VSWITCH_EVENT0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_VSWITCH_EVENT0_
 - fwpmtypes/FWPM_VSWITCH_EVENT0_
 - FWPM_VSWITCH_EVENT0
 - fwpmtypes/FWPM_VSWITCH_EVENT0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_VSWITCH_EVENT0
---

## -description

The <b>FWPM_VSWITCH_EVENT0</b> structure contains information about a vSwitch event.

## -struct-fields

### -field eventType

Type: [FWPM_VSWITCH_EVENT_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)</b>

The type of vSwitch event.

### -field vSwitchId

Type: <b>wchar_t*</b>

GUID that identifies a vSwitch.

### -field positionInfo

Available when <b>eventType</b> is <b>FWPM_VSWITCH_EVENT_FILTER_ADD_TO_FILTER_ENGINE_NOT_IN_REQUIRED_POSITION</b>.

### -field positionInfo.numvSwitchFilterExtensions

Type: <b>ULONG</b>

The number of vSwitch filter extensions.

### -field positionInfo.vSwitchFilterExtensions

Type: <b>LPWSTR*</b>

size_is(numvSwitchFilterExtensions)

Array of strings identifying other vSwitch extensions.

### -field reorderInfo

Available when <b>eventType</b> is <b>FWPM_VSWITCH_EVENT_FILTER_ENGINE_REORDER</b>.

### -field reorderInfo.inRequiredPosition

Type: <b>BOOL</b>

True if the filter engine is in the required position to correctly enforce committed filters; otherwise, false.

### -field reorderInfo.numvSwitchFilterExtensions

Type: <b>ULONG</b>

The number of vSwitch filter extensions.

### -field reorderInfo.vSwitchFilterExtensions

Type: <b>LPWSTR*</b>

size_is(numvSwitchFilterExtensions)

Array of strings identifying other vSwitch extensions.

## -remarks

For the unnamed union, switch_is(eventType), switch_type(FWPM_VSWITCH_EVENT_TYPE).

<b>FWPM_VSWITCH_EVENT0</b> is a specific implementation of FWPM_VSWITCH_EVENT. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.

## -see-also

[FWPM_VSWITCH_EVENT_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
