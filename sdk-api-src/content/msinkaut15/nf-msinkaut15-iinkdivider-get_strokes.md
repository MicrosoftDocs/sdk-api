---
UID: NF:msinkaut15.IInkDivider.get_Strokes
title: IInkDivider::get_Strokes
author: windows-sdk-content
description: Gets or sets the InkStrokes collection on which the InkDivider object performs layout analysis.
old-location: tablet\inkdivider_strokes.htm
old-project: tablet
ms.assetid: 611ccce9-7acb-4138-9655-938efcaa4c75
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 611ccce9-7acb-4138-9655-938efcaa4c75, IInkDivider interface [Tablet PC],Strokes property, IInkDivider.Strokes, IInkDivider.get_Strokes, IInkDivider::Strokes, IInkDivider::get_Strokes, IInkDivider::putref_Strokes, InkDivider.get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkDivider interface, get_Strokes, msinkaut15/IInkDivider::Strokes, msinkaut15/IInkDivider::get_Strokes, msinkaut15/IInkDivider::putref_Strokes, tablet.inkdivider_strokes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: InkRecoGuide
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
product: Windows
targetos: Windows
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDivider::get_Strokes


## -description



Gets or sets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection on which the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object performs layout analysis.



This property is read/write.


## -parameters


## -remarks



This property maintains the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection which the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object analyzes and from which the <b>InkDivider</b> object creates the <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object. This property must be assigned a InkStrokes collection in order for the <b>InkDivider</b> object to perform layout analysis.

You should only assign this property once to a given <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object. Assigning a subsequent <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> object once one has been assigned will cause inaccurate results to be returned. Also, you may not change the <a href="https://msdn.microsoft.com/69e65ad6-bcee-46a7-a139-80b4324b9c72">LineHeight</a> or <a href="https://msdn.microsoft.com/ad3c4317-a777-4009-bc66-865a2fcb77c3">RecognizerContext</a> property after a InkStrokes collection is assigned to the <b>Strokes</b> property.

To keep the <b>Strokes</b> property of the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object synchronized with an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, use the <a href="https://msdn.microsoft.com/46bbdb98-524f-4b4b-95c0-005e71d672f1">InkAdded</a> and <a href="https://msdn.microsoft.com/59ada470-6620-411d-889e-882f41ccea3e">InkDeleted</a> events of the <b>InkDisp</b> object to listen for strokes that should be added or removed from the <b>InkDivider</b> object. This covers cases where strokes are added to, deleted from, clipped, or split within the <b>InkDisp</b> object.

<div class="alert"><b>Note</b>  Moving, scaling, or other transformations on strokes in the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object do not generate <a href="https://msdn.microsoft.com/46bbdb98-524f-4b4b-95c0-005e71d672f1">InkAdded</a> or <a href="https://msdn.microsoft.com/59ada470-6620-411d-889e-882f41ccea3e">InkDeleted</a> events. Perform the same transformations on the strokes in the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object to keep the <b>Strokes</b> property of the <b>InkDivider</b> object synchronized.</div>
<div> </div>



## -see-also




<a href="tablet.iinkdivider">IInkDivider</a>



<a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

