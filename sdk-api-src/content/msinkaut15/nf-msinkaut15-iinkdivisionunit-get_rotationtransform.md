---
UID: NF:msinkaut15.IInkDivisionUnit.get_RotationTransform
title: IInkDivisionUnit::get_RotationTransform
author: windows-sdk-content
description: Gets the transformation matrix that the IInkDivisionUnit object uses to rotate the strokes to horizontal.
old-location: tablet\iinkdivisionunit_rotationtransform.htm
old-project: tablet
ms.assetid: 2c1c0b5e-2f39-4901-a8c7-96dd65ced5c8
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 2c1c0b5e-2f39-4901-a8c7-96dd65ced5c8, IInkDivisionUnit interface [Tablet PC],RotationTransform property, IInkDivisionUnit.RotationTransform, IInkDivisionUnit.get_RotationTransform, IInkDivisionUnit::RotationTransform, IInkDivisionUnit::get_RotationTransform, RotationTransform property [Tablet PC], RotationTransform property [Tablet PC],IInkDivisionUnit interface, get_RotationTransform, msinkaut15/IInkDivisionUnit::RotationTransform, msinkaut15/IInkDivisionUnit::get_RotationTransform, tablet.iinkdivisionunit_rotationtransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut15.h
req.include-header: 
req.redist: 
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
 - IInkDivisionUnit.RotationTransform
 - IInkDivisionUnit.get_RotationTransform
 - IInkDivisionUnit.get_RotationTransform
product: Windows
targetos: Windows
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDivisionUnit::get_RotationTransform


## -description



Gets the transformation matrix that the <a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit</a> object uses to rotate the strokes to horizontal.



This property is read-only.


## -parameters


## -remarks



Text recognizers
           perform best with horizontal handwriting. Apply this transformation to the <a href="https://msdn.microsoft.com/b65f1b71-b0a4-4de2-9321-f660bcd2d3ce">Strokes</a> property of the <a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit</a> object before passing the strokes to an <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.

<div class="alert"><b>Note</b>  For an <a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit</a> object which represents a paragraph or drawing, this property returns <b>NULL</b>.</div>
<div> </div>
Use this property to level handwriting or to accurately draw lines or shapes around angled handwriting.




## -see-also




<a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit Interface</a>



<a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform Class</a>
 

 

