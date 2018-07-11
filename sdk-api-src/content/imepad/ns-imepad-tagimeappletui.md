---
UID: NS:imepad.tagIMEAPPLETUI
title: tagIMEAPPLETUI
author: windows-sdk-content
description: Used by IImePadApplet::CreateUI to specify applet window style.
old-location: intl\imeappletui.htm
old-project: Intl
ms.assetid: 9C44287B-77A9-48FB-8A17-6CB0FA234EE2
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: "*LPIMEAPPLETUI, IMEAPPLETUI, IMEAPPLETUI structure [Internationalization for Windows Applications], PIMEAPPLETUI, PIMEAPPLETUI structure pointer [Internationalization for Windows Applications], imepad/IMEAPPLETUI, imepad/PIMEAPPLETUI, intl.imeappletui, tagIMEAPPLETUI"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMEAPPLETUI, *LPIMEAPPLETUI
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imepad.h
api_name:
 - IMEAPPLETUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagIMEAPPLETUI structure


## -description


Used by <a href="https://msdn.microsoft.com/B4F79A20-E69E-4EA0-A992-4415B8AA4790">IImePadApplet::CreateUI</a> to specify applet window style.


## -struct-fields




### -field hwnd

Window handle created by applet window.


### -field dwStyle

Applet window style. The style is a combination of <b>IPAWS_*</b> flags; see the Remarks of <a href="https://msdn.microsoft.com/C74B0374-D6C7-44C7-94EF-E97B46534462">IImePad::Request</a> for the possible <b>IPAWS_*</b> flags.


### -field width

The applet window's initial width.


### -field height

The applet window's initial height.


### -field minWidth

Minimum width of the applet window. Valid only when <b>IPAWS_MINWIDTHFIXED</b> style is set in <i>dwStyle</i>.


### -field minHeight

Minimum height of applet window. Valid only when <b>IPAWS_MINHEIGHTFIXED</b> is set in <i>dwStyle</i>.


### -field maxWidth

Maximum width of applet window. Valid only when <b>IPAWS_MAXWIDTHFIXED</b> is set in <i>dwStyle</i>.


### -field maxHeight

Maximum height of applet window. Valid only when <b>IPAWS_MAXHEIGHTFIXED</b> is set in <i>dwStyle</i>.


### -field lReserved1

Reserved.


### -field lReserved2

Reserved.

