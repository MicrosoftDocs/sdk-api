---
UID: NS:mmc._MMCButton
title: MMCBUTTON (mmc.h)
description: The MMCBUTTON structure contains values used in creating buttons on a toolbar. This structure is similar to the TBBUTTON structure discussed in the Platform Software Development Kit (SDK) topics related to common controls.
helpviewer_keywords: ["*LPMMCBUTTON","LPMMCBUTTON","LPMMCBUTTON structure pointer [MMC]","MMCBUTTON","MMCBUTTON structure [MMC]","TBSTATE_CHECKED","TBSTATE_ENABLED","TBSTATE_HIDDEN","TBSTATE_INDETERMINATE","TBSTATE_PRESSED","TBSTYLE_BUTTON","TBSTYLE_CHECK","TBSTYLE_CHECKGROUP","TBSTYLE_GROUP","TBSTYLE_SEP","_slate_mmcbutton","mmc.mmcbutton","mmc/LPMMCBUTTON","mmc/MMCBUTTON"]
old-location: mmc\mmcbutton.htm
tech.root: mmc
ms.assetid: 340fed49-3003-4dd6-80c9-6cefc8c5b750
ms.date: 12/05/2018
ms.keywords: '*LPMMCBUTTON, LPMMCBUTTON, LPMMCBUTTON structure pointer [MMC], MMCBUTTON, MMCBUTTON structure [MMC], TBSTATE_CHECKED, TBSTATE_ENABLED, TBSTATE_HIDDEN, TBSTATE_INDETERMINATE, TBSTATE_PRESSED, TBSTYLE_BUTTON, TBSTYLE_CHECK, TBSTYLE_CHECKGROUP, TBSTYLE_GROUP, TBSTYLE_SEP, _slate_mmcbutton, mmc.mmcbutton, mmc/LPMMCBUTTON, mmc/MMCBUTTON'
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
req.typenames: MMCBUTTON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMCButton
 - mmc/_MMCButton
 - MMCBUTTON
 - mmc/MMCBUTTON
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
 - MMCBUTTON
---

# MMCBUTTON structure


## -description

The 
<b>MMCBUTTON</b> structure contains values used in creating buttons on a toolbar. This structure is similar to the <b>TBBUTTON</b> structure discussed in the Platform Software Development Kit (SDK) topics related to common controls.

## -struct-fields

### -field nBitmap

A value that specifies the zero-based index of a button image.

### -field idCommand

A value that specifies the command identifier returned when a button is clicked. This can be any integer value the user wants. Only the low word of the <b>int</b> is used.

### -field fsState

A value that specifies the button-state flags. This member can be any of the following values:



#### TBSTATE_CHECKED

The button has the TBSTYLE_CHECKED style and is being pressed.



#### TBSTATE_ENABLED

The button accepts user input. A button that does not have this state does not accept user input and appears dimmed.



#### TBSTATE_HIDDEN

The button is not visible and cannot receive user input.



#### TBSTATE_INDETERMINATE

The button appears dimmed.



#### TBSTATE_PRESSED

The button is being pressed.

### -field fsType

A value that specifies the button style. This member can be any combination of the following values:



#### TBSTYLE_BUTTON

Creates a standard push button.



#### TBSTYLE_CHECK

Creates a button that toggles between the pressed and not-pressed states each time the user clicks it. The button has a different background color when it is in the pressed state.



#### TBSTYLE_CHECKGROUP

Creates a check button that stays pressed until another button in the group is pressed.



#### TBSTYLE_GROUP

Creates a button that stays pressed until another button in the group is pressed.



#### TBSTYLE_SEP

Creates a separator, providing a small gap between button groups. A button that has this style does not receive user input.

### -field lpButtonText

A pointer to the text associated with a particular instance of the 
<b>MMCBUTTON</b> structure.

### -field lpTooltipText

A pointer to the text for a particular tooltip.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>