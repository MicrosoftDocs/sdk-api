---
UID: NF:dwmapi.DwmShowContact
title: DwmShowContact function (dwmapi.h)
description: Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.
helpviewer_keywords: ["DWMSC_ALL","DWMSC_DOWN","DWMSC_DRAG","DWMSC_HOLD","DWMSC_NONE","DWMSC_PENBARREL","DWMSC_UP","DwmShowContact","DwmShowContact function [Desktop Window Manager]","dwm.DwmShowContact","dwmapi/DwmShowContact"]
old-location: dwm\DwmShowContact.htm
tech.root: dwm
ms.assetid: E9C302AA-D622-483d-83AC-0D0D7D23719E
ms.date: 12/05/2018
ms.keywords: DWMSC_ALL, DWMSC_DOWN, DWMSC_DRAG, DWMSC_HOLD, DWMSC_NONE, DWMSC_PENBARREL, DWMSC_UP, DwmShowContact, DwmShowContact function [Desktop Window Manager], dwm.DwmShowContact, dwmapi/DwmShowContact
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmShowContact
 - dwmapi/DwmShowContact
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - Dwmapi.dll
 - API-MS-Win-dwmapi-l1-1-0.dll
 - Ext-Ms-Win-DwmAPI-Ext-L1-1-0.dll
api_name:
 - DwmShowContact
---

# DwmShowContact function


## -description

Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.

## -parameters

### -param dwPointerID [in]

The pointer ID of the contact. Each touch or pen contact is given a unique ID when it is detected.

### -param eShowContact [in]

One or more of the following DWM_SHOWCONTACT visualizations that DWM should show for this contact.

#### DWMSC_NONE (0x00000000)

No visual feedback should be shown in response to the contact.

#### DWMSC_DOWN (0x00000001)

Show the "contact down" animation, such as would be used in a button press.

#### DWMSC_UP (0x00000002)

Show the "contact up" animation, such as would be used in a button release.

#### DWMSC_DRAG (0x00000004)

Show the "contact drag" animation when the UI element that was selected by the touch or pen is dragged.

#### DWMSC_HOLD (0x00000008)

Show a visual while the contact is held down, such as holding down a button.

#### DWMSC_PENBARREL (0x00000010)

Show the pen barrel visual when the pen barrel button is pressed.

#### DWMSC_ALL (0xFFFFFFFF)

Show any of the animations if called for.

## -returns

If <i>dwPointerID</i> does not match that of a contact currently present on the screen, this function returns E_INVALIDARG; otherwise, it returns S_OK.

## -remarks

It is safe to call this function on the UI thread.

