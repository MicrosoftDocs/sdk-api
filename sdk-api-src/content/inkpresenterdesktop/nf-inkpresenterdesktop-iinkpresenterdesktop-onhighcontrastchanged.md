---
UID: NF:inkpresenterdesktop.IInkPresenterDesktop.OnHighContrastChanged
title: IInkPresenterDesktop::OnHighContrastChanged (inkpresenterdesktop.h)
description: Specifies a high contrast change handler. This handler is notified of changes to the high contrast system settings.
helpviewer_keywords: ["IInkPresenterDesktop interface","OnHighContrastChanged method","IInkPresenterDesktop.OnHighContrastChanged","IInkPresenterDesktop::OnHighContrastChanged","InkPresenterDesktop.iinkpresenterdesktop_onhighcontrastchanged","OnHighContrastChanged","OnHighContrastChanged method","OnHighContrastChanged method","IInkPresenterDesktop interface","inkpresenterdesktop/IInkPresenterDesktop::OnHighContrastChanged","input_ink.iinkpresenterdesktop_onhighcontrastchanged"]
old-location: input_ink\iinkpresenterdesktop_onhighcontrastchanged.htm
tech.root: input_ink
ms.assetid: f231fbb7-685b-49db-80c5-dee367ff7f5b
ms.date: 12/05/2018
ms.keywords: IInkPresenterDesktop interface,OnHighContrastChanged method, IInkPresenterDesktop.OnHighContrastChanged, IInkPresenterDesktop::OnHighContrastChanged, InkPresenterDesktop.iinkpresenterdesktop_onhighcontrastchanged, OnHighContrastChanged, OnHighContrastChanged method, OnHighContrastChanged method,IInkPresenterDesktop interface, inkpresenterdesktop/IInkPresenterDesktop::OnHighContrastChanged, input_ink.iinkpresenterdesktop_onhighcontrastchanged
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
 - IInkPresenterDesktop::OnHighContrastChanged
 - inkpresenterdesktop/IInkPresenterDesktop::OnHighContrastChanged
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
 - IInkPresenterDesktop.OnHighContrastChanged
---

# IInkPresenterDesktop::OnHighContrastChanged

## -description

Specifies a high contrast change handler. This handler is notified of changes to the high contrast system settings in Windows 10 and earlier (Settings -> Ease of Access -> High Contrast -> Use high contrast).

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

IInkPresenterDesktop
[Complex ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk)
[Simple ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk)
[Ink renderer interfaces](/windows/win32/input_ink/ink-renderer-interfaces)
[Pen and stylus interactions](/windows/uwp/input-and-devices/pen-and-stylus-interactions)
