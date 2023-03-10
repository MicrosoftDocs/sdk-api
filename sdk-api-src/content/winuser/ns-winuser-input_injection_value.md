---
UID: NS:winuser.tagINPUT_INJECTION_VALUE
title: INPUT_INJECTION_VALUE (winuser.h)
description: Contains the input injection details.
helpviewer_keywords: ["*PINPUT_INJECTION_VALUE","INPUT_INJECTION_VALUE","INPUT_INJECTION_VALUE structure","PINPUT_INJECTION_VALUE","PINPUT_INJECTION_VALUE structure pointer","input_pointerdevice.input_injection_value","winuser/INPUT_INJECTION_VALUE","winuser/PINPUT_INJECTION_VALUE"]
old-location: input_pointerdevice\input_injection_value.htm
tech.root: controls
ms.assetid: 8F639719-A098-4850-933D-F84DEA412242
ms.date: 12/05/2018
ms.keywords: '*PINPUT_INJECTION_VALUE, INPUT_INJECTION_VALUE, INPUT_INJECTION_VALUE structure, PINPUT_INJECTION_VALUE, PINPUT_INJECTION_VALUE structure pointer, input_pointerdevice.input_injection_value, winuser/INPUT_INJECTION_VALUE, winuser/PINPUT_INJECTION_VALUE'
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: INPUT_INJECTION_VALUE, *PINPUT_INJECTION_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagINPUT_INJECTION_VALUE
 - winuser/tagINPUT_INJECTION_VALUE
 - PINPUT_INJECTION_VALUE
 - winuser/PINPUT_INJECTION_VALUE
 - INPUT_INJECTION_VALUE
 - winuser/INPUT_INJECTION_VALUE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - INPUT_INJECTION_VALUE
---

# INPUT_INJECTION_VALUE structure


## -description

Contains the  input injection details.

## -struct-fields

### -field page

The Usage Page ID, such as VR Controls Page (0x03) or Game Controls Page (0x05).

### -field usage

 The Usage ID associated with a Usage Page, such as Turn Right/Left (21) or Move Right/Left (24) for a Game Controls Page.

### -field value

The injected input value.

### -field index

The Usage index, such as the selected item in a  radio button set.

## -see-also

<a href="https://www.usb.org/sites/default/files/documents/hut1_12v2.pdf">Universal Serial Bus HID Usage Tables - USB.org</a>

