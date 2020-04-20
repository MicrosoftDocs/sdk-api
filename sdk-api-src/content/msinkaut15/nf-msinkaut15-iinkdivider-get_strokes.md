---
UID: NF:msinkaut15.IInkDivider.get_Strokes
title: IInkDivider::get_Strokes (msinkaut15.h)
description: Gets or sets the InkStrokes collection on which the InkDivider object performs layout analysis.helpviewer_keywords: ["611ccce9-7acb-4138-9655-938efcaa4c75","IInkDivider interface [Tablet PC]","Strokes property","IInkDivider.Strokes","IInkDivider.get_Strokes","IInkDivider::Strokes","IInkDivider::get_Strokes","IInkDivider::putref_Strokes","InkDivider.get_Strokes","Strokes property [Tablet PC]","Strokes property [Tablet PC]","IInkDivider interface","get_Strokes","msinkaut15/IInkDivider::Strokes","msinkaut15/IInkDivider::get_Strokes","msinkaut15/IInkDivider::putref_Strokes","tablet.inkdivider_strokes"]
old-location: tablet\inkdivider_strokes.htm
tech.root: tablet
ms.assetid: 611ccce9-7acb-4138-9655-938efcaa4c75
ms.date: 12/05/2018
ms.keywords: 611ccce9-7acb-4138-9655-938efcaa4c75, IInkDivider interface [Tablet PC],Strokes property, IInkDivider.Strokes, IInkDivider.get_Strokes, IInkDivider::Strokes, IInkDivider::get_Strokes, IInkDivider::putref_Strokes, InkDivider.get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkDivider interface, get_Strokes, msinkaut15/IInkDivider::Strokes, msinkaut15/IInkDivider::get_Strokes, msinkaut15/IInkDivider::putref_Strokes, tablet.inkdivider_strokes
f1_keywords:
- msinkaut15/IInkDivider.Strokes
dev_langs:
- c++
req.header: msinkaut15.h
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
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
api_name:
- IInkDivider.Strokes
- IInkDivider.get_Strokes
- InkDivider.get_Strokes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDivider::get_Strokes


## -description



Gets or sets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection on which the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object performs layout analysis.



This property is read/write.


## -parameters


## -remarks



This property maintains the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection which the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object analyzes and from which the <b>InkDivider</b> object creates the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object. This property must be assigned a InkStrokes collection in order for the <b>InkDivider</b> object to perform layout analysis.

You should only assign this property once to a given <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object. Assigning a subsequent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> object once one has been assigned will cause inaccurate results to be returned. Also, you may not change the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight">LineHeight</a> or <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext">RecognizerContext</a> property after a InkStrokes collection is assigned to the <b>Strokes</b> property.

To keep the <b>Strokes</b> property of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object synchronized with an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, use the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkadded">InkAdded</a> and <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkdeleted">InkDeleted</a> events of the <b>InkDisp</b> object to listen for strokes that should be added or removed from the <b>InkDivider</b> object. This covers cases where strokes are added to, deleted from, clipped, or split within the <b>InkDisp</b> object.

<div class="alert"><b>Note</b>  Moving, scaling, or other transformations on strokes in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object do not generate <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkadded">InkAdded</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-inkdeleted">InkDeleted</a> events. Perform the same transformations on the strokes in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object to keep the <b>Strokes</b> property of the <b>InkDivider</b> object synchronized.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt847144(v=VS.85).aspx">IInkDivider</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider Class</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
 

 

