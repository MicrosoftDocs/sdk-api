---
UID: NN:msinkaut.IInkRecognitionAlternates
title: IInkRecognitionAlternates (msinkaut.h)
description: Contains the IInkRecognitionAlternate objects that represent possible word matches for segments of ink.
helpviewer_keywords: ["39f49762-de86-4a1a-ac7b-327b65c3eb54","IInkRecognitionAlternates","IInkRecognitionAlternates interface [Tablet PC]","IInkRecognitionAlternates interface [Tablet PC]","described","msinkaut/IInkRecognitionAlternates","tablet.iinkrecognitionalternates"]
old-location: tablet\iinkrecognitionalternates.htm
tech.root: tablet
ms.assetid: 39f49762-de86-4a1a-ac7b-327b65c3eb54
ms.date: 12/05/2018
ms.keywords: 39f49762-de86-4a1a-ac7b-327b65c3eb54, IInkRecognitionAlternates, IInkRecognitionAlternates interface [Tablet PC], IInkRecognitionAlternates interface [Tablet PC],described, msinkaut/IInkRecognitionAlternates, tablet.iinkrecognitionalternates
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
 - IInkRecognitionAlternates
 - msinkaut/IInkRecognitionAlternates
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
 - IInkRecognitionAlternates
 - IInkRecognitionAlternates._NewEnum
---

# IInkRecognitionAlternates interface


## -description

Contains the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> objects that represent possible word matches for segments of ink.

## -inheritance

The <b>IInkRecognitionAlternates</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognitionAlternates</b> also has these types of members:

## -remarks

For more information about collections in COM, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
