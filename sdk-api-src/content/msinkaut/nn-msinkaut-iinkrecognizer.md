---
UID: NN:msinkaut.IInkRecognizer
title: IInkRecognizer (msinkaut.h)
description: Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an InkRecognizerContext object, which is used to perform the actual handwriting recognition.
helpviewer_keywords: ["97f982b6-f330-4053-91a9-2a4edc13b4b0","IInkRecognizer","IInkRecognizer interface [Tablet PC]","IInkRecognizer interface [Tablet PC]","described","msinkaut/IInkRecognizer","tablet.iinkrecognizer"]
old-location: tablet\iinkrecognizer.htm
tech.root: tablet
ms.assetid: 97f982b6-f330-4053-91a9-2a4edc13b4b0
ms.date: 12/05/2018
ms.keywords: 97f982b6-f330-4053-91a9-2a4edc13b4b0, IInkRecognizer, IInkRecognizer interface [Tablet PC], IInkRecognizer interface [Tablet PC],described, msinkaut/IInkRecognizer, tablet.iinkrecognizer
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
 - IInkRecognizer
 - msinkaut/IInkRecognizer
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
 - IInkRecognizer
---

# IInkRecognizer interface


## -description

Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object, which is used to perform the actual handwriting recognition.

## -inheritance

The <b>IInkRecognizer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognizer</b> also has these types of members:

## -remarks

A recognizer has specific attributes and properties that allow it to perform recognition. The properties of a recognizer must be determined before recognition can occur. The types of properties that a recognizer supports determine the types of recognition it can perform. For instance, if a recognizer doesn't support cursive handwriting, it returns inaccurate results when a user writes in cursive.

A recognizer also has built-in functionality that automatically manages many aspects of handwriting. For instance, it determines the metrics for the lines on which strokes are drawn. You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.

For more information about recognition, see <a href="/windows/desktop/tablet/about-handwriting-recognition">About Handwriting Recognition</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)">InkRecognizers Collection</a>
