---
UID: NF:msinkaut.IInkRecognizerContext.putref_Strokes
title: IInkRecognizerContext::putref_Strokes (msinkaut.h)
description: Gets or sets the InkStrokes collection associated with the InkRecognizerContext object.helpviewer_keywords: ["IInkRecognizerContext interface [Tablet PC]","Strokes property","IInkRecognizerContext.Strokes","IInkRecognizerContext.putref_Strokes","IInkRecognizerContext::Strokes","IInkRecognizerContext::get_Strokes","IInkRecognizerContext::putref_Strokes","InkRecognizerContext.get_Strokes","Strokes property [Tablet PC]","Strokes property [Tablet PC]","IInkRecognizerContext interface","af31559b-741e-4af2-8c35-9e34ad1af85f","get_Strokes","msinkaut/IInkRecognizerContext::Strokes","msinkaut/IInkRecognizerContext::get_Strokes","msinkaut/IInkRecognizerContext::putref_Strokes","putref_Strokes","tablet.inkrecognizercontext_strokes"]
old-location: tablet\inkrecognizercontext_strokes.htm
tech.root: tablet
ms.assetid: af31559b-741e-4af2-8c35-9e34ad1af85f
ms.date: 12/05/2018
ms.keywords: IInkRecognizerContext interface [Tablet PC],Strokes property, IInkRecognizerContext.Strokes, IInkRecognizerContext.putref_Strokes, IInkRecognizerContext::Strokes, IInkRecognizerContext::get_Strokes, IInkRecognizerContext::putref_Strokes, InkRecognizerContext.get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkRecognizerContext interface, af31559b-741e-4af2-8c35-9e34ad1af85f, get_Strokes, msinkaut/IInkRecognizerContext::Strokes, msinkaut/IInkRecognizerContext::get_Strokes, msinkaut/IInkRecognizerContext::putref_Strokes, putref_Strokes, tablet.inkrecognizercontext_strokes
f1_keywords:
- msinkaut/IInkRecognizerContext.Strokes
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkRecognizerContext.Strokes
- IInkRecognizerContext.get_Strokes
- InkRecognizerContext.get_Strokes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizerContext::putref_Strokes


## -description



Gets or sets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection associated with the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.



This property is read/write.


## -parameters


## -remarks



You can set the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection more than once. Each time you set the InkStrokes collection, the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object is reset-any ink or results are removed and any prior calls to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput">EndInkInput Method</a> method are disregarded-and then the new strokes are added.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection can also be set to <b>NULL</b>, which also resets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object. When the <b>InkRecognizerContext</b> is reset, it keeps any guides, factoids, and other properties which previously had been set on it.

When the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object is reset, any recognition taking place on the background thread is canceled.

To keep the <b>Strokes</b> property of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object synchronized with an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, use the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkadded">InkAdded</a> and <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkdeleted">InkDeleted</a> events of the <b>InkDisp</b> object to listen for strokes that should be added or removed from the <b>InkRecognizerContext</b> object. This covers cases where strokes are added to, deleted from, clipped, or split within the <b>InkDisp</b> object.

<div class="alert"><b>Note</b>  Moving, scaling, or other transformations on strokes in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object do not generate <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkadded">InkAdded</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkdeleted">InkDeleted</a> events. Perform the same transformations on the strokes in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object to keep the <b>Strokes</b> property of the <b>InkRecognizerContext</b> object synchronized.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846801(v=VS.85).aspx">IInkRecognizerContext</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
 

 

