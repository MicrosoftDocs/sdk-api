---
UID: NN:ddraw.IDirectDrawColorControl
title: IDirectDrawColorControl (ddraw.h)
description: Applications use the methods of the IDirectDrawColorControl interface to get and set color controls.
helpviewer_keywords: ["IDirectDrawColorControl","IDirectDrawColorControl interface [DirectDraw]","IDirectDrawColorControl interface [DirectDraw]","described","ddraw/IDirectDrawColorControl","directdraw.idirectdrawcolorcontrol"]
old-location: directdraw\idirectdrawcolorcontrol.htm
tech.root: directdraw
ms.assetid: e9bd0dc6-2d8a-452b-894d-72a3d7a20100
ms.date: 12/05/2018
ms.keywords: IDirectDrawColorControl, IDirectDrawColorControl interface [DirectDraw], IDirectDrawColorControl interface [DirectDraw],described, ddraw/IDirectDrawColorControl, directdraw.idirectdrawcolorcontrol
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawColorControl
 - ddraw/IDirectDrawColorControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawColorControl
---

# IDirectDrawColorControl interface


## -description

Applications use the methods of the <b>IDirectDrawColorControl</b> interface to get and set color controls.

## -inheritance

The <b>IDirectDrawColorControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawColorControl</b> also has these types of members:

## -remarks

You can use the LPDIRECTDRAWCOLORCONTROL data type to declare a variable that contains a pointer to an <b>IDirectDrawColorControl</b> interface. The Ddraw.h header file declares this data type with the following code:




```

typedef struct IDirectDrawColorControl    FAR *LPDIRECTDRAWCOLORCONTROL;

```
