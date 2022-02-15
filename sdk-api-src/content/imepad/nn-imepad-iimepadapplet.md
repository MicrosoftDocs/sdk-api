---
UID: NN:imepad.IImePadApplet
title: IImePadApplet (imepad.h)
description: The IImePadApplet interface inputs strings into apps through the IImePad interface.
helpviewer_keywords: ["IImePadApplet","IImePadApplet interface [Internationalization for Windows Applications]","IImePadApplet interface [Internationalization for Windows Applications]","described","imepad/IImePadApplet","intl.iimepadapplet"]
old-location: intl\iimepadapplet.htm
tech.root: Intl
ms.assetid: F3BC7176-9659-47B6-AFCA-049807394961
ms.date: 12/05/2018
ms.keywords: IImePadApplet, IImePadApplet interface [Internationalization for Windows Applications], IImePadApplet interface [Internationalization for Windows Applications],described, imepad/IImePadApplet, intl.iimepadapplet
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
 - IImePadApplet
 - imepad/IImePadApplet
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
 - IImePadApplet
---

# IImePadApplet interface


## -description

The <b>IImePadApplet</b> interface inputs strings into apps through the <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface.

<b>IImePadApplet</b> should be implemented as a DLL inproc server. The developer can implement multiple <b>IImePadApplet</b> interfaces in one DLL.  To specify and emulate the <b>IImePadApplet</b> interface in the applet DLL, the applet must also provide the <a href="/windows/desktop/api/imepad/nn-imepad-iimespecifyapplets">IImeSpecifyApplets</a> interface.

## -inheritance

The <b>IImePadApplet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImePadApplet</b> also has these types of members:

