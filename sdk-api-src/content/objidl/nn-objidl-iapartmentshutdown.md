---
UID: NN:objidl.IApartmentShutdown
title: IApartmentShutdown (objidl.h)
description: Enables registration of an apartment shutdown notification handler.
helpviewer_keywords: ["IApartmentShutdown","IApartmentShutdown interface [Windows Runtime]","IApartmentShutdown interface [Windows Runtime]","described","objidl/IApartmentShutdown","winrt.iapartmentshutdown"]
old-location: winrt\iapartmentshutdown.htm
tech.root: WinRT
ms.assetid: 28EDAC77-5175-4AF7-A06C-B735336AAD9B
ms.date: 12/05/2018
ms.keywords: IApartmentShutdown, IApartmentShutdown interface [Windows Runtime], IApartmentShutdown interface [Windows Runtime],described, objidl/IApartmentShutdown, winrt.iapartmentshutdown
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IApartmentShutdown
 - objidl/IApartmentShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IApartmentShutdown
---

# IApartmentShutdown interface


## -description

Enables registration of  an apartment shutdown notification handler.

## -inheritance

The <b>IApartmentShutdown</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApartmentShutdown</b> also has these types of members:

## -remarks

Implement the <b>IApartmentShutdown</b> interface to use the <a href="/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a> function.

## -see-also

<a href="/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a>
