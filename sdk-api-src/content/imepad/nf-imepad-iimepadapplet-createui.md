---
UID: NF:imepad.IImePadApplet.CreateUI
title: IImePadApplet::CreateUI (imepad.h)
description: Called from IImePad to get the applet's window handle, style, and size.
helpviewer_keywords: ["CreateUI","CreateUI method [Internationalization for Windows Applications]","CreateUI method [Internationalization for Windows Applications]","IImePadApplet interface","IImePadApplet interface [Internationalization for Windows Applications]","CreateUI method","IImePadApplet.CreateUI","IImePadApplet::CreateUI","imepad/IImePadApplet::CreateUI","intl.iimepadapplet_createui"]
old-location: intl\iimepadapplet_createui.htm
tech.root: Intl
ms.assetid: B4F79A20-E69E-4EA0-A992-4415B8AA4790
ms.date: 12/05/2018
ms.keywords: CreateUI, CreateUI method [Internationalization for Windows Applications], CreateUI method [Internationalization for Windows Applications],IImePadApplet interface, IImePadApplet interface [Internationalization for Windows Applications],CreateUI method, IImePadApplet.CreateUI, IImePadApplet::CreateUI, imepad/IImePadApplet::CreateUI, intl.iimepadapplet_createui
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImePadApplet::CreateUI
 - imepad/IImePadApplet::CreateUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImePadApplet.CreateUI
---

# IImePadApplet::CreateUI


## -description

Called from <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> to get the applet's window handle, style, and size.

The applet can set its window style and  sizing policy.

## -parameters

### -param hwndParent [in]

Window handle of the <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> GUI. The applet can create the window as its child window.

### -param lpImeAppletUI [in]

Pointer to <a href="/windows/desktop/api/imepad/ns-imepad-imeappletui">IMEAPPLETUI</a> structure. The applet can set its window style.

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a>