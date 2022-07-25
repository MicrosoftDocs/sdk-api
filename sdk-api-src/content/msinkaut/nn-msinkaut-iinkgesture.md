---
UID: NN:msinkaut.IInkGesture
title: IInkGesture (msinkaut.h)
description: Represents the ability to query particular properties of a gesture returned from a gesture recognition.
helpviewer_keywords: ["87a1db34-371e-4c02-a470-55f35dfbf4ab","IInkGesture","IInkGesture interface [Tablet PC]","IInkGesture interface [Tablet PC]","described","msinkaut/IInkGesture","tablet.iinkgesture"]
old-location: tablet\iinkgesture.htm
tech.root: tablet
ms.assetid: 87a1db34-371e-4c02-a470-55f35dfbf4ab
ms.date: 12/05/2018
ms.keywords: 87a1db34-371e-4c02-a470-55f35dfbf4ab, IInkGesture, IInkGesture interface [Tablet PC], IInkGesture interface [Tablet PC],described, msinkaut/IInkGesture, tablet.iinkgesture
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkGesture
 - msinkaut/IInkGesture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkGesture
---

# IInkGesture interface


## -description

Represents the ability to query particular properties of a gesture returned from a gesture recognition.

## -inheritance

The <b>IInkGesture</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkGesture</b> also has these types of members:

## -remarks

Gesture support is built-in by using the Microsoft gesture recognizer. Available gestures are found in the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture</a> enumeration type. For more information about gestures, see <a href="/windows/desktop/tablet/using-gestures">Using Gestures</a> and <a href="/previous-versions/windows/desktop/ms702526(v=vs.85)">Command Input on the Tablet PC</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture">InkSystemGesture Enumeration</a>
