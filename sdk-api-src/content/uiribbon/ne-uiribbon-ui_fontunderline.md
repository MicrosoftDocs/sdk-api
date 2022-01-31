---
UID: NE:uiribbon.UI_FONTUNDERLINE
title: UI_FONTUNDERLINE (uiribbon.h)
description: Specifies values that identify the underline state of a FontControl.
helpviewer_keywords: ["UI_FONTUNDERLINE","UI_FONTUNDERLINE enumeration [Windows Ribbon]","UI_FONTUNDERLINE_NOTAVAILABLE","UI_FONTUNDERLINE_NOTSET","UI_FONTUNDERLINE_SET","scenicintent_UI_FONTUNDERLINE","uiribbon/UI_FONTUNDERLINE","uiribbon/UI_FONTUNDERLINE_NOTAVAILABLE","uiribbon/UI_FONTUNDERLINE_NOTSET","uiribbon/UI_FONTUNDERLINE_SET","windowsribbon.windowsribbon_ui_fontunderline"]
old-location: windowsribbon\windowsribbon_ui_fontunderline.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_fontunderline.htm
ms.date: 12/05/2018
ms.keywords: UI_FONTUNDERLINE, UI_FONTUNDERLINE enumeration [Windows Ribbon], UI_FONTUNDERLINE_NOTAVAILABLE, UI_FONTUNDERLINE_NOTSET, UI_FONTUNDERLINE_SET, scenicintent_UI_FONTUNDERLINE, uiribbon/UI_FONTUNDERLINE, uiribbon/UI_FONTUNDERLINE_NOTAVAILABLE, uiribbon/UI_FONTUNDERLINE_NOTSET, uiribbon/UI_FONTUNDERLINE_SET, windowsribbon.windowsribbon_ui_fontunderline
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
req.typenames: UI_FONTUNDERLINE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_FONTUNDERLINE
 - uiribbon/UI_FONTUNDERLINE
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
 - UI_FONTUNDERLINE
---

# UI_FONTUNDERLINE enumeration


## -description

Specifies values that identify the underline state of a <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a>.

## -enum-fields

### -field UI_FONTUNDERLINE_NOTAVAILABLE:0

Underlining is not enabled.

### -field UI_FONTUNDERLINE_NOTSET:1

Underlining is off.

### -field UI_FONTUNDERLINE_SET:2

Underlining is on.

## -remarks

<b>UI_FONTUNDERLINE</b> is associated with the <b>Underline</b> toggle button of the <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a> as shown in the following screen shot.

<img alt="Screen shot of the FontControl element with the RichFont attribute set to true." src="./images/FontControl_Underline.png"/>
The <b>Underline</b> toggle button is displayed by default in a <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a> but can be hidden, depending on the value of the <i>FontType</i> attribute.

The <b>Underline</b> button is toggled based on the <b>UI_FONTUNDERLINE</b> value in <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-underline">UI_PKEY_FontProperties_Underline</a>.

A solid single line is the only underline style supported by the <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a>.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-underline">UI_PKEY_FontProperties_Underline</a>
