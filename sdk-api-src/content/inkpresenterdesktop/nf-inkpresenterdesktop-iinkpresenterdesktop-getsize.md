---
UID: NF:inkpresenterdesktop.IInkPresenterDesktop.GetSize
title: IInkPresenterDesktop::GetSize (inkpresenterdesktop.h)
description: Gets the size of the InkPresenter object.
helpviewer_keywords: ["GetSize","GetSize method","GetSize method","IInkPresenterDesktop interface","IInkPresenterDesktop interface","GetSize method","IInkPresenterDesktop.GetSize","IInkPresenterDesktop::GetSize","InkPresenterDesktop.iinkpresenterdesktop_getsize","inkpresenterdesktop/IInkPresenterDesktop::GetSize","input_ink.iinkpresenterdesktop_getsize"]
old-location: input_ink\iinkpresenterdesktop_getsize.htm
tech.root: input_ink
ms.assetid: d4ce0503-72dc-4a25-a48d-58fa50c5047f
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method, GetSize method,IInkPresenterDesktop interface, IInkPresenterDesktop interface,GetSize method, IInkPresenterDesktop.GetSize, IInkPresenterDesktop::GetSize, InkPresenterDesktop.iinkpresenterdesktop_getsize, inkpresenterdesktop/IInkPresenterDesktop::GetSize, input_ink.iinkpresenterdesktop_getsize
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
 - IInkPresenterDesktop::GetSize
 - inkpresenterdesktop/IInkPresenterDesktop::GetSize
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
 - IInkPresenterDesktop.GetSize
---

# IInkPresenterDesktop::GetSize


## -description

Gets the size of the <a href="https://msdn.microsoft.com/561e2d14-288a-490a-9a3b-5a32e98b51c3">InkPresenter</a> object.

## -parameters

### -param width [out]

The width of the object, in DIPs.

### -param height [out]

The height of the object, in DIPs.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex ink sample</a>



<a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a>






<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>

<a href="https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex Ink sample</a>

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk">Simple ink sample</a>