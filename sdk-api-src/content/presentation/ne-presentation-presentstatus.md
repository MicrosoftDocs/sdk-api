---
UID: NE:presentation.PresentStatus
tech.root: comp_swapchain
title: PresentStatus
ms.date: 06/08/2021
targetos: Windows
description: Defines constants that specify the status of a present.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: presentation.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - PresentStatus
f1_keywords:
 - PresentStatus
 - presentation/PresentStatus
dev_langs:
 - c++
---

## -description

## -enum-fields

Defines constants that specify the status of a present.

### -field PresentStatus_Queued

The frame was queued by the system to eventually be shown.

### -field PresentStatus_Skipped

The frame was skipped because a later frame was a better candidate to show.

### -field PresentStatus_Canceled

The frame arrived, but was canceled by the application, so it was not displayed.

## -remarks

The status of a present indicates how it was handled based on timing, and whether it was canceled.

## -see-also

