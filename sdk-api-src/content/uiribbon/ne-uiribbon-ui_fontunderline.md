---
UID: NE:uiribbon.UI_FONTUNDERLINE
title: UI_FONTUNDERLINE
author: windows-sdk-content
description: Specifies values that identify the underline state of a FontControl.
old-location: windowsribbon\windowsribbon_ui_fontunderline.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_fontunderline.htm
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: UI_FONTUNDERLINE, UI_FONTUNDERLINE enumeration [Windows Ribbon], UI_FONTUNDERLINE_NOTAVAILABLE, UI_FONTUNDERLINE_NOTSET, UI_FONTUNDERLINE_SET, scenicintent_UI_FONTUNDERLINE, uiribbon/UI_FONTUNDERLINE, uiribbon/UI_FONTUNDERLINE_NOTAVAILABLE, uiribbon/UI_FONTUNDERLINE_NOTSET, uiribbon/UI_FONTUNDERLINE_SET, windowsribbon.windowsribbon_ui_fontunderline
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
tech.root: 
req.typenames: UI_FONTUNDERLINE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_FONTUNDERLINE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UI_FONTUNDERLINE enumeration


## -description


Specifies values that identify the underline state of a <a href="https://msdn.microsoft.com/library/Dd371673(v=VS.85).aspx">FontControl</a>.


## -enum-fields




### -field UI_FONTUNDERLINE_NOTAVAILABLE

Underlining is not enabled.


### -field UI_FONTUNDERLINE_NOTSET

Underlining is off.


### -field UI_FONTUNDERLINE_SET

Underlining is on.


## -remarks



<b>UI_FONTUNDERLINE</b> is associated with the <b>Underline</b> toggle button of the <a href="https://msdn.microsoft.com/library/Dd371673(v=VS.85).aspx">FontControl</a> as shown in the following screen shot.

<img alt="Screen shot of the FontControl element with the RichFont attribute set to true." src="./images/Markup/FontControl_Underline.png"/>
The <b>Underline</b> toggle button is displayed by default in a <a href="https://msdn.microsoft.com/library/Dd371673(v=VS.85).aspx">FontControl</a> but can be hidden, depending on the value of the <i>FontType</i> attribute.

The <b>Underline</b> button is toggled based on the <b>UI_FONTUNDERLINE</b> value in <a href="https://msdn.microsoft.com/library/Dd371236(v=VS.85).aspx">UI_PKEY_FontProperties_Underline</a>.

A solid single line is the only underline style supported by the <a href="https://msdn.microsoft.com/library/Dd371673(v=VS.85).aspx">FontControl</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Dd371540(v=VS.85).aspx">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/library/Dd371236(v=VS.85).aspx">UI_PKEY_FontProperties_Underline</a>
 

 

