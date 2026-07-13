---
UID: NE:uiribbon.UI_FONTVERTICALPOSITION
title: UI_FONTVERTICALPOSITION (uiribbon.h)
description: Specifies values that identify the vertical-alignment state of a FontControl.
helpviewer_keywords: ["UI_FONTVERTICALPOSITION","UI_FONTVERTICALPOSITION enumeration [Windows Ribbon]","UI_FONTVERTICALPOSITION_NOTAVAILABLE","UI_FONTVERTICALPOSITION_NOTSET","UI_FONTVERTICALPOSITION_SUBSCRIPT","UI_FONTVERTICALPOSITION_SUPERSCRIPT","scenicintent_UI_FONTVERTICALPOSITION","uiribbon/UI_FONTVERTICALPOSITION","uiribbon/UI_FONTVERTICALPOSITION_NOTAVAILABLE","uiribbon/UI_FONTVERTICALPOSITION_NOTSET","uiribbon/UI_FONTVERTICALPOSITION_SUBSCRIPT","uiribbon/UI_FONTVERTICALPOSITION_SUPERSCRIPT","windowsribbon.windowsribbon_ui_fontverticalposition"]
old-location: windowsribbon\windowsribbon_ui_fontverticalposition.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_fontverticalposition.htm
ms.date: 12/05/2018
ms.keywords: UI_FONTVERTICALPOSITION, UI_FONTVERTICALPOSITION enumeration [Windows Ribbon], UI_FONTVERTICALPOSITION_NOTAVAILABLE, UI_FONTVERTICALPOSITION_NOTSET, UI_FONTVERTICALPOSITION_SUBSCRIPT, UI_FONTVERTICALPOSITION_SUPERSCRIPT, scenicintent_UI_FONTVERTICALPOSITION, uiribbon/UI_FONTVERTICALPOSITION, uiribbon/UI_FONTVERTICALPOSITION_NOTAVAILABLE, uiribbon/UI_FONTVERTICALPOSITION_NOTSET, uiribbon/UI_FONTVERTICALPOSITION_SUBSCRIPT, uiribbon/UI_FONTVERTICALPOSITION_SUPERSCRIPT, windowsribbon.windowsribbon_ui_fontverticalposition
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
req.typenames: UI_FONTVERTICALPOSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_FONTVERTICALPOSITION
 - uiribbon/UI_FONTVERTICALPOSITION
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
 - UI_FONTVERTICALPOSITION
---

# UI_FONTVERTICALPOSITION enumeration


## -description

Specifies values that identify the vertical-alignment state of a <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a>.

## -enum-fields

### -field UI_FONTVERTICALPOSITION_NOTAVAILABLE:0

Vertical positioning is not enabled.

### -field UI_FONTVERTICALPOSITION_NOTSET:1

Vertical positioning is enabled but not toggled.

### -field UI_FONTVERTICALPOSITION_SUPERSCRIPT:2

Vertical positioning is enabled and toggled for superscript.

### -field UI_FONTVERTICALPOSITION_SUBSCRIPT:3

Vertical positioning is enabled and toggled for subscript.

## -remarks

<b>UI_FONTVERTICALPOSITION</b> is associated with the <b>Subscript</b> and <b>Superscript</b> toggle buttons of the <i>RichFont</i> <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a> as shown in the following screen shot.

<img alt="Screen shot of the FontControl element with the RichFont attribute set to true." src="./images/FontControl_SubSuper.png"/>
The <b>Subscript</b> and <b>Superscript</b> toggle buttons  are displayed by default in a <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a>, depending on the value of the <i>FontType</i> attribute. 

The <b>Subscript</b> and <b>Superscript</b> buttons are toggled based on the <b>UI_FONTVERTICALPOSITION</b> value in <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning">UI_PKEY_FontProperties_VerticalPositioning</a>.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning">UI_PKEY_FontProperties_VerticalPositioning</a>
