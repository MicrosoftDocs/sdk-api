---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

