---
UID: NS:winuser.tagUSAGE_PROPERTIES
title: USAGE_PROPERTIES (winuser.h)
description: Contains device properties (Human Interface Device (HID) global items that correspond to HID usages) for any type of HID input device.
helpviewer_keywords: ["*PUSAGE_PROPERTIES","PUSAGE_PROPERTIES","PUSAGE_PROPERTIES structure pointer","USAGE_PROPERTIES","USAGE_PROPERTIES structure","input_pointerdevice.usage_properties","winuser/PUSAGE_PROPERTIES","winuser/USAGE_PROPERTIES"]
old-location: input_pointerdevice\usage_properties.htm
tech.root: controls
ms.assetid: 387E241E-2FE9-46C0-9B7C-5357731339BF
ms.date: 12/05/2018
ms.keywords: '*PUSAGE_PROPERTIES, PUSAGE_PROPERTIES, PUSAGE_PROPERTIES structure pointer, USAGE_PROPERTIES, USAGE_PROPERTIES structure, input_pointerdevice.usage_properties, winuser/PUSAGE_PROPERTIES, winuser/USAGE_PROPERTIES'
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
req.typenames: USAGE_PROPERTIES, *PUSAGE_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUSAGE_PROPERTIES
 - winuser/tagUSAGE_PROPERTIES
 - PUSAGE_PROPERTIES
 - winuser/PUSAGE_PROPERTIES
 - USAGE_PROPERTIES
 - winuser/USAGE_PROPERTIES
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
 - USAGE_PROPERTIES
---

# USAGE_PROPERTIES structure


## -description

Contains device properties (Human Interface Device (HID) global items that correspond to HID usages) for any type of HID input device.

## -struct-fields

### -field level

A usage-specific value for a range-based linear control (knob or dial), an on/off  control (toggle switch), a momentary control (mouse button), a one-shot control (button that triggers a single event), or re-trigger control (button that triggers a repeating event).

### -field page

The Usage Page ID, such as VR Controls Page (0x03) or Game Controls Page (0x05).

### -field usage

 The Usage ID associated with a Usage Page, such as Turn Right/Left (21) or Move Right/Left (24) for a Game Controls Page.

### -field logicalMinimum

The smallest value that the control can report.

### -field logicalMaximum

The largest value that the control can report.

### -field unit

The standard of measure used to describe a control's physical value (after converting the logical value using the <i>exponent</i> value). The HID specification defines codes for the basic units of length, mass, time, temperature, current, and luminous intensity.

### -field exponent

The value used to scale a logical value to a physical value.

### -field count

 The number of data
items contained in the report.

### -field physicalMinimum

The <i>logicalMinimum</i> expressed in physical units (converted by multiplying <i>logicalMinimum</i> by <i>exponent</i>).

### -field physicalMaximum

The <i>logicalMaximum</i> expressed in physical units (converted by multiplying <i>logicalMaximum</i> by <i>exponent</i>).

## -remarks

The HID working group publishes a set of documents that make up the HID Usage Tables (the dictionary that describes what HID devices are allowed to do). These HID Usage Tables contain a list with Usage descriptions. A Usage provides information to an application developer about the intended meaning and use of a particular item described in the Report Descriptor. For example, there is a Usage defined for the left button of a mouse. The Report Descriptor can define where in a report an application can find the current state of the mouse’s left button. The Usage Tables are broken up into several name spaces, called Usage Pages. Each Usage Page describes a set of related Usages to help organize the document. The combination of a Usage Page and Usage defines the Usage ID that uniquely identifies a specific Usage in the Usage Tables.

## -see-also

<a href="https://www.usb.org/sites/default/files/documents/hut1_12v2.pdf">Universal Serial Bus HID Usage Tables - USB.org</a>

