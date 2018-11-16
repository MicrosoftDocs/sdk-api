---
UID: NF:imepad.IImePadApplet.CreateUI
title: IImePadApplet::CreateUI
author: windows-sdk-content
description: Called from IImePad to get the applet's window handle, style, and size.
old-location: intl\iimepadapplet_createui.htm
tech.root: Intl
ms.assetid: B4F79A20-E69E-4EA0-A992-4415B8AA4790
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateUI, CreateUI method [Internationalization for Windows Applications], CreateUI method [Internationalization for Windows Applications],IImePadApplet interface, IImePadApplet interface [Internationalization for Windows Applications],CreateUI method, IImePadApplet.CreateUI, IImePadApplet::CreateUI, imepad/IImePadApplet::CreateUI, intl.iimepadapplet_createui
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImePadApplet.CreateUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imepad.h
: 
- IImePadApplet.CreateUI
: 
---

# IImePadApplet::CreateUI


## -description


Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to get the applet's window handle, style, and size.

The applet can set its window style and  sizing policy.


## -parameters




### -param hwndParent [in]

Window handle of the <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> GUI. The applet can create the window as its child window.


### -param lpImeAppletUI [in]

Pointer to <a href="https://msdn.microsoft.com/9C44287B-77A9-48FB-8A17-6CB0FA234EE2">IMEAPPLETUI</a> structure. The applet can set its window style.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a>
 

 

