---
UID: NF:msinkaut15.IInkDivider.get_RecognizerContext
title: IInkDivider::get_RecognizerContext
author: windows-sdk-content
description: Gets or sets the InkRecognizerContext object that the InkDivider object uses for layout analysis.
old-location: tablet\inkdivider_recognizercontext.htm
tech.root: tablet
ms.assetid: ad3c4317-a777-4009-bc66-865a2fcb77c3
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IInkDivider interface [Tablet PC],RecognizerContext property, IInkDivider.RecognizerContext, IInkDivider.get_RecognizerContext, IInkDivider::RecognizerContext, IInkDivider::get_RecognizerContext, IInkDivider::putref_RecognizerContext, InkDivider.get_RecognizerContext, RecognizerContext property [Tablet PC], RecognizerContext property [Tablet PC],IInkDivider interface, ad3c4317-a777-4009-bc66-865a2fcb77c3, get_RecognizerContext, msinkaut15/IInkDivider::RecognizerContext, msinkaut15/IInkDivider::get_RecognizerContext, msinkaut15/IInkDivider::putref_RecognizerContext, put_RecognizerContext, tablet.inkdivider_recognizercontext
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInkDivider.RecognizerContext
 - IInkDivider.get_RecognizerContext
 - InkDivider.get_RecognizerContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDivider::get_RecognizerContext


## -description



Gets or sets the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object that the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object uses for layout analysis.



This property is read/write.


## -parameters


## -remarks



If you set the <b>RecognizerContext</b> property, it should be the first thing you do after constructing the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object. An error is generated if you attempt to set the <b>RecognizerContext</b> property after the <a href="https://msdn.microsoft.com/611ccce9-7acb-4138-9655-938efcaa4c75">Divider.Strokes</a> property has been set, after a <a href="https://msdn.microsoft.com/be42ac65-2bde-4439-a82b-3453c0737717">Divider.Divide</a> call has been made, or if you attempt to set it more than one time.

In addition, this property generates an error if you assign a recognizer context to it that:

<ul>
<li>Is not a text recognizer.</li>
<li>Does not free support.</li>
</ul>
If the value of this property is <b>NULL</b> when strokes are assigned to the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object, then the <b>InkDivider</b> object uses no recognizer context.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object uses the default property settings of the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object, and ignores any strokes assigned to the <b>InkRecognizerContext</b> object.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6DF54C8E-1E0D-4F9D-A6E4-AFE0E8894BE9">IInkDivider</a>



<a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider Class</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

