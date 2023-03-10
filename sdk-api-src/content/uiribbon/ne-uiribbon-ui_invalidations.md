---
UID: NE:uiribbon.UI_INVALIDATIONS
title: UI_INVALIDATIONS (uiribbon.h)
description: Specifies values that identify the aspect of a Command to invalidate.
helpviewer_keywords: ["UI_INVALIDATIONS","UI_INVALIDATIONS enumeration [Windows Ribbon]","UI_INVALIDATIONS_ALLPROPERTIES","UI_INVALIDATIONS_PROPERTY","UI_INVALIDATIONS_STATE","UI_INVALIDATIONS_VALUE","scenicintent_UI_INVALIDATIONS","uiribbon/UI_INVALIDATIONS","uiribbon/UI_INVALIDATIONS_ALLPROPERTIES","uiribbon/UI_INVALIDATIONS_PROPERTY","uiribbon/UI_INVALIDATIONS_STATE","uiribbon/UI_INVALIDATIONS_VALUE","windowsribbon.windowsribbon_ui_invalidations"]
old-location: windowsribbon\windowsribbon_ui_invalidations.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_invalidations.htm
ms.date: 12/05/2018
ms.keywords: UI_INVALIDATIONS, UI_INVALIDATIONS enumeration [Windows Ribbon], UI_INVALIDATIONS_ALLPROPERTIES, UI_INVALIDATIONS_PROPERTY, UI_INVALIDATIONS_STATE, UI_INVALIDATIONS_VALUE, scenicintent_UI_INVALIDATIONS, uiribbon/UI_INVALIDATIONS, uiribbon/UI_INVALIDATIONS_ALLPROPERTIES, uiribbon/UI_INVALIDATIONS_PROPERTY, uiribbon/UI_INVALIDATIONS_STATE, uiribbon/UI_INVALIDATIONS_VALUE, windowsribbon.windowsribbon_ui_invalidations
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UI_INVALIDATIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_INVALIDATIONS
 - uiribbon/UI_INVALIDATIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_INVALIDATIONS
---

# UI_INVALIDATIONS enumeration


## -description

Specifies values that identify the aspect of a Command to invalidate.

## -enum-fields

### -field UI_INVALIDATIONS_STATE:0x1

A state property, such as <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-enabled">UI_PKEY_Enabled</a>.

### -field UI_INVALIDATIONS_VALUE:0x2

The value property of a Command.

### -field UI_INVALIDATIONS_PROPERTY:0x4

Any property.

### -field UI_INVALIDATIONS_ALLPROPERTIES:0x8

All properties.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand">IUIFramework::InvalidateUICommand</a>
