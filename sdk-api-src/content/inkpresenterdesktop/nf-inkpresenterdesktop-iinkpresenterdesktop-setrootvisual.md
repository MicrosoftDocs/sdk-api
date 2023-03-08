---
UID: NF:inkpresenterdesktop.IInkPresenterDesktop.SetRootVisual
title: IInkPresenterDesktop::SetRootVisual (inkpresenterdesktop.h)
description: Sets the connection to the app's DirectComposition visual tree.
helpviewer_keywords: ["IInkPresenterDesktop interface","SetRootVisual method","IInkPresenterDesktop.SetRootVisual","IInkPresenterDesktop::SetRootVisual","InkPresenterDesktop.iinkpresenterdesktop_setrootvisual","SetRootVisual","SetRootVisual method","SetRootVisual method","IInkPresenterDesktop interface","inkpresenterdesktop/IInkPresenterDesktop::SetRootVisual","input_ink.iinkpresenterdesktop_setrootvisual"]
old-location: input_ink\iinkpresenterdesktop_setrootvisual.htm
tech.root: input_ink
ms.assetid: 27b08f20-d43b-452c-809d-837664eb42d0
ms.date: 12/05/2018
ms.keywords: IInkPresenterDesktop interface,SetRootVisual method, IInkPresenterDesktop.SetRootVisual, IInkPresenterDesktop::SetRootVisual, InkPresenterDesktop.iinkpresenterdesktop_setrootvisual, SetRootVisual, SetRootVisual method, SetRootVisual method,IInkPresenterDesktop interface, inkpresenterdesktop/IInkPresenterDesktop::SetRootVisual, input_ink.iinkpresenterdesktop_setrootvisual
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
 - IInkPresenterDesktop::SetRootVisual
 - inkpresenterdesktop/IInkPresenterDesktop::SetRootVisual
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
 - IInkPresenterDesktop.SetRootVisual
---

# IInkPresenterDesktop::SetRootVisual


## -description

Sets the connection to the app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree.

## -parameters

### -param rootVisual [in]

The app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree.

### -param device [in]

NULL for default ink rendering, or an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a> object used to commit all pending DirectComposition commands for custom drying of ink input to the app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex ink sample</a>



<a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a>






<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>

<a href="https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex Ink sample</a>

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk">Simple ink sample</a>