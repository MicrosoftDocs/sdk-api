---
UID: NF:inkpresenterdesktop.IInkDesktopHost.CreateAndInitializeInkPresenter
title: IInkDesktopHost::CreateAndInitializeInkPresenter (inkpresenterdesktop.h)
description: Creates an IInkPresenterDesktop object on an application thread, connects it to the app's DirectComposition visual tree, and sets the size of the object.
helpviewer_keywords: ["CreateAndInitializeInkPresenter","CreateAndInitializeInkPresenter method","CreateAndInitializeInkPresenter method","IInkDesktopHost interface","IInkDesktopHost interface","CreateAndInitializeInkPresenter method","IInkDesktopHost.CreateAndInitializeInkPresenter","IInkDesktopHost::CreateAndInitializeInkPresenter","InkPresenterDesktop.iinkdesktophost_createandinitializeinkpresenter","inkpresenterdesktop/IInkDesktopHost::CreateAndInitializeInkPresenter","input_ink.iinkdesktophost_createandinitializeinkpresenter"]
old-location: input_ink\iinkdesktophost_createandinitializeinkpresenter.htm
tech.root: input_ink
ms.assetid: 596e1180-04ca-474b-b519-f9ebe468fb6a
ms.date: 12/05/2018
ms.keywords: CreateAndInitializeInkPresenter, CreateAndInitializeInkPresenter method, CreateAndInitializeInkPresenter method,IInkDesktopHost interface, IInkDesktopHost interface,CreateAndInitializeInkPresenter method, IInkDesktopHost.CreateAndInitializeInkPresenter, IInkDesktopHost::CreateAndInitializeInkPresenter, InkPresenterDesktop.iinkdesktophost_createandinitializeinkpresenter, inkpresenterdesktop/IInkDesktopHost::CreateAndInitializeInkPresenter, input_ink.iinkdesktophost_createandinitializeinkpresenter
req.header: inkpresenterdesktop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InkPresenterDesktop.idl
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
 - IInkDesktopHost::CreateAndInitializeInkPresenter
 - inkpresenterdesktop/IInkDesktopHost::CreateAndInitializeInkPresenter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkPresenterDesktop.h
api_name:
 - IInkDesktopHost.CreateAndInitializeInkPresenter
---

# IInkDesktopHost::CreateAndInitializeInkPresenter


## -description

Creates an <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a> object on an application thread, connects it to the app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree, and sets the size of the object.

## -parameters

### -param rootVisual [in]

The <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a> of the app.

### -param width [in]

The width, in pixels, of the inking area.

### -param height [in]

The height, in pixels, of the inking area.

### -param riid [in]

A reference to the interface identifier of an <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a> object.

### -param ppv [out]

Address of a pointer variable that receives the interface pointer identified by <i>riid</i>.

## -returns

If successful, returns the requested interface pointer. Otherwise, returns <b>NULL</b>.

## -see-also

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex ink sample</a>



<a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost">IInkDesktopHost</a>





<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>

<a href="https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex Ink sample</a>



<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk">Simple ink sample</a>