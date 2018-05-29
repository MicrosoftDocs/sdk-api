---
UID: NE:uiribbon.UI_FONTVERTICALPOSITION
title: UI_FONTVERTICALPOSITION
author: windows-sdk-content
description: Specifies values that identify the vertical-alignment state of a FontControl.
old-location: windowsribbon\windowsribbon_ui_fontverticalposition.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_fontverticalposition.htm
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: UI_FONTVERTICALPOSITION, UI_FONTVERTICALPOSITION enumeration [Windows Ribbon], UI_FONTVERTICALPOSITION_NOTAVAILABLE, UI_FONTVERTICALPOSITION_NOTSET, UI_FONTVERTICALPOSITION_SUBSCRIPT, UI_FONTVERTICALPOSITION_SUPERSCRIPT, scenicintent_UI_FONTVERTICALPOSITION, uiribbon/UI_FONTVERTICALPOSITION, uiribbon/UI_FONTVERTICALPOSITION_NOTAVAILABLE, uiribbon/UI_FONTVERTICALPOSITION_NOTSET, uiribbon/UI_FONTVERTICALPOSITION_SUBSCRIPT, uiribbon/UI_FONTVERTICALPOSITION_SUPERSCRIPT, windowsribbon.windowsribbon_ui_fontverticalposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: UI_FONTVERTICALPOSITION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Uiribbon.h
api_name:
-	UI_FONTVERTICALPOSITION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UI_FONTVERTICALPOSITION enumeration


## -description


Specifies values that identify the vertical-alignment state of a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a>.


## -enum-fields




### -field UI_FONTVERTICALPOSITION_NOTAVAILABLE

Vertical positioning is not enabled.


### -field UI_FONTVERTICALPOSITION_NOTSET

Vertical positioning is enabled but not toggled.


### -field UI_FONTVERTICALPOSITION_SUPERSCRIPT

Vertical positioning is enabled and toggled for superscript.


### -field UI_FONTVERTICALPOSITION_SUBSCRIPT

Vertical positioning is enabled and toggled for subscript.


## -remarks



<b>UI_FONTVERTICALPOSITION</b> is associated with the <b>Subscript</b> and <b>Superscript</b> toggle buttons of the <i>RichFont</i> <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a> as shown in the following screen shot.

<img alt="Screen shot of the FontControl element with the RichFont attribute set to true." src="images/Markup/FontControl_SubSuper.png"/>
The <b>Subscript</b> and <b>Superscript</b> toggle buttons  are displayed by default in a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a>, depending on the value of the <i>FontType</i> attribute. 

The <b>Subscript</b> and <b>Superscript</b> buttons are toggled based on the <b>UI_FONTVERTICALPOSITION</b> value in <a href="https://msdn.microsoft.com/a92f845e-b0fc-4e23-9d06-ca16d2becf0b">UI_PKEY_FontProperties_VerticalPositioning</a>.




## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/a92f845e-b0fc-4e23-9d06-ca16d2becf0b">UI_PKEY_FontProperties_VerticalPositioning</a>
 

 

