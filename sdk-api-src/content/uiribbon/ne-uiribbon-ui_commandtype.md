---
UID: NE:uiribbon.UI_COMMANDTYPE
title: UI_COMMANDTYPE (uiribbon.h)
description: Specifies values that identify the type of Command associated with a Ribbon control.
helpviewer_keywords: ["UI_COMMANDTYPE","UI_COMMANDTYPE enumeration [Windows Ribbon]","UI_COMMANDTYPE_ACTION","UI_COMMANDTYPE_ANCHOR","UI_COMMANDTYPE_BOOLEAN","UI_COMMANDTYPE_COLLECTION","UI_COMMANDTYPE_COLORANCHOR","UI_COMMANDTYPE_COLORCOLLECTION","UI_COMMANDTYPE_COMMANDCOLLECTION","UI_COMMANDTYPE_CONTEXT","UI_COMMANDTYPE_DECIMAL","UI_COMMANDTYPE_FONT","UI_COMMANDTYPE_GROUP","UI_COMMANDTYPE_RECENTITEMS","UI_COMMANDTYPE_UNKNOWN","scenicintent_UI_COMMANDTYPE","uiribbon/UI_COMMANDTYPE","uiribbon/UI_COMMANDTYPE_ACTION","uiribbon/UI_COMMANDTYPE_ANCHOR","uiribbon/UI_COMMANDTYPE_BOOLEAN","uiribbon/UI_COMMANDTYPE_COLLECTION","uiribbon/UI_COMMANDTYPE_COLORANCHOR","uiribbon/UI_COMMANDTYPE_COLORCOLLECTION","uiribbon/UI_COMMANDTYPE_COMMANDCOLLECTION","uiribbon/UI_COMMANDTYPE_CONTEXT","uiribbon/UI_COMMANDTYPE_DECIMAL","uiribbon/UI_COMMANDTYPE_FONT","uiribbon/UI_COMMANDTYPE_GROUP","uiribbon/UI_COMMANDTYPE_RECENTITEMS","uiribbon/UI_COMMANDTYPE_UNKNOWN","windowsribbon.windowsribbon_ui_commandtype"]
old-location: windowsribbon\windowsribbon_ui_commandtype.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_commandtype.htm
ms.date: 12/05/2018
ms.keywords: UI_COMMANDTYPE, UI_COMMANDTYPE enumeration [Windows Ribbon], UI_COMMANDTYPE_ACTION, UI_COMMANDTYPE_ANCHOR, UI_COMMANDTYPE_BOOLEAN, UI_COMMANDTYPE_COLLECTION, UI_COMMANDTYPE_COLORANCHOR, UI_COMMANDTYPE_COLORCOLLECTION, UI_COMMANDTYPE_COMMANDCOLLECTION, UI_COMMANDTYPE_CONTEXT, UI_COMMANDTYPE_DECIMAL, UI_COMMANDTYPE_FONT, UI_COMMANDTYPE_GROUP, UI_COMMANDTYPE_RECENTITEMS, UI_COMMANDTYPE_UNKNOWN, scenicintent_UI_COMMANDTYPE, uiribbon/UI_COMMANDTYPE, uiribbon/UI_COMMANDTYPE_ACTION, uiribbon/UI_COMMANDTYPE_ANCHOR, uiribbon/UI_COMMANDTYPE_BOOLEAN, uiribbon/UI_COMMANDTYPE_COLLECTION, uiribbon/UI_COMMANDTYPE_COLORANCHOR, uiribbon/UI_COMMANDTYPE_COLORCOLLECTION, uiribbon/UI_COMMANDTYPE_COMMANDCOLLECTION, uiribbon/UI_COMMANDTYPE_CONTEXT, uiribbon/UI_COMMANDTYPE_DECIMAL, uiribbon/UI_COMMANDTYPE_FONT, uiribbon/UI_COMMANDTYPE_GROUP, uiribbon/UI_COMMANDTYPE_RECENTITEMS, uiribbon/UI_COMMANDTYPE_UNKNOWN, windowsribbon.windowsribbon_ui_commandtype
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
req.typenames: UI_COMMANDTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_COMMANDTYPE
 - uiribbon/UI_COMMANDTYPE
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
 - UI_COMMANDTYPE
---

# UI_COMMANDTYPE enumeration


## -description

Specifies values that identify the type of Command associated with a Ribbon control.

## -enum-fields

### -field UI_COMMANDTYPE_UNKNOWN:0

The type of command is not known.

### -field UI_COMMANDTYPE_GROUP:1

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-group">Group</a>

### -field UI_COMMANDTYPE_ACTION:2

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-button">Button</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-helpbutton">Help Button</a>

### -field UI_COMMANDTYPE_ANCHOR:3

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-applicationmenu">Application Menu</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-dropdownbutton">Drop-Down Button</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-splitbutton">Split Button</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-tab">Tab</a>

### -field UI_COMMANDTYPE_CONTEXT:4

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-tabgroup">Tab Group</a>

### -field UI_COMMANDTYPE_COLLECTION:5

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-combobox">Combo Box</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-dropdowngallery">Drop-Down Gallery</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-inribbongallery">In-Ribbon Gallery</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-splitbuttongallery">Split Button Gallery</a>

### -field UI_COMMANDTYPE_COMMANDCOLLECTION:6

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-dropdowngallery">Drop-Down Gallery</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-inribbongallery">In-Ribbon Gallery</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-quickaccesstoolbar">Quick Access Toolbar</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-splitbuttongallery">Split Button Gallery</a>

### -field UI_COMMANDTYPE_DECIMAL:7

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-spinner">Spinner</a>

### -field UI_COMMANDTYPE_BOOLEAN:8

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-togglebutton">Toggle Button</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-controls-checkbox">Check Box</a>

### -field UI_COMMANDTYPE_FONT:9

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-fontcontrol">Font Control</a>

### -field UI_COMMANDTYPE_RECENTITEMS:10

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-recentitems">Recent Items</a>

### -field UI_COMMANDTYPE_COLORANCHOR:11

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-dropdowncolorpicker">Drop-Down Color Picker</a>

### -field UI_COMMANDTYPE_COLORCOLLECTION:12

This Command type is not supported by any framework controls.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>
