---
UID: NF:msinkaut.IInkRecognizerContext.get_Factoid
title: IInkRecognizerContext::get_Factoid (msinkaut.h)
description: Gets or sets the factoid that a recognizer uses to constrain its search for the recognition result. (Get)
helpviewer_keywords: ["11a76706-e2e5-4ae5-bdc2-5354514ea29f","Factoid property [Tablet PC]","Factoid property [Tablet PC]","IInkRecognizerContext interface","IInkRecognizerContext interface [Tablet PC]","Factoid property","IInkRecognizerContext.Factoid","IInkRecognizerContext.get_Factoid","IInkRecognizerContext::Factoid","IInkRecognizerContext::get_Factoid","IInkRecognizerContext::put_Factoid","InkRecognizerContext.get_Factoid","InkRecognizerContext.put_Factoid","get_Factoid","msinkaut/IInkRecognizerContext::Factoid","msinkaut/IInkRecognizerContext::get_Factoid","msinkaut/IInkRecognizerContext::put_Factoid","put_Factoid","tablet.inkrecognizercontext_factoid"]
old-location: tablet\inkrecognizercontext_factoid.htm
tech.root: tablet
ms.assetid: 11a76706-e2e5-4ae5-bdc2-5354514ea29f
ms.date: 12/05/2018
ms.keywords: 11a76706-e2e5-4ae5-bdc2-5354514ea29f, Factoid property [Tablet PC], Factoid property [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],Factoid property, IInkRecognizerContext.Factoid, IInkRecognizerContext.get_Factoid, IInkRecognizerContext::Factoid, IInkRecognizerContext::get_Factoid, IInkRecognizerContext::put_Factoid, InkRecognizerContext.get_Factoid, InkRecognizerContext.put_Factoid, get_Factoid, msinkaut/IInkRecognizerContext::Factoid, msinkaut/IInkRecognizerContext::get_Factoid, msinkaut/IInkRecognizerContext::put_Factoid, put_Factoid, tablet.inkrecognizercontext_factoid
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
 - IInkRecognizerContext::get_Factoid
 - msinkaut/IInkRecognizerContext::get_Factoid
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
 - IInkRecognizerContext.Factoid
 - IInkRecognizerContext.get_Factoid
 - IInkRecognizerContext.put_Factoid
 - InkRecognizerContext.get_Factoid
 - InkRecognizerContext.put_Factoid
---

# IInkRecognizerContext::get_Factoid


## -description

Gets or sets the factoid that a recognizer uses to constrain its search for the recognition result.



This property is read/write.

## -parameters

## -remarks

A factoid provides recognizer context for recognized ink in the context of a particular field. You specify a factoid if an input field is of a known type, for example, if the input field contains a date.

For more information about factoids and how to use them, see <a href="/windows/desktop/tablet/using-context-to-improve-accuracy">Improving Tablet PC Recognition Accuracy by Setting Context</a>.

Setting the <b>Factoid</b> succeeds only if the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection is <b>NULL</b>. You must set the <b>Factoid</b> before you attach the InkStrokes collection to the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> or you must set the Strokes collection to <b>NULL</b> and then set the <b>Factoid</b> (and possibly reattach the InkStrokes collection).

To ensure that ink is recognized in the correct field context, set this property before processing the ink for the first time, such as before calling the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize">Recognize</a> method.

<div class="alert"><b>Note</b>  All factoids are case sensitive.</div>
<div> </div>
This property takes or returns a string parameter and not a class object of the <a href="/windows/desktop/tablet/factoid-constants">Factoid</a> class. The members of this class are of type <b>string</b>.

For the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, this property should only be changed if the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a> property returns <a href="/windows/desktop/api/inked/ne-inked-inkeditstatus">IES_Idle</a>.

## -see-also

<a href="/windows/desktop/tablet/factoid-constants">Factoid Constants</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>
