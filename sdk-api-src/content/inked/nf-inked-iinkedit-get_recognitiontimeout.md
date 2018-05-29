---
UID: NF:inked.IInkEdit.get_RecognitionTimeout
title: IInkEdit::get_RecognitionTimeout
author: windows-sdk-content
description: Gets or sets the length of time, in milliseconds, between the last IInkStrokeDisp object collected and the beginning of text recognition.
old-location: tablet\inkedit_recotimeout.htm
old-project: tablet
ms.assetid: e1171aa3-841f-433e-88b8-e3fc63129aeb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IInkEdit interface [Tablet PC],RecognitionTimeout property, IInkEdit.RecognitionTimeout, IInkEdit.get_RecognitionTimeout, IInkEdit::RecognitionTimeout, IInkEdit::get_RecognitionTimeout, IInkEdit::put_RecognitionTimeout, InkEdit.get_RecognitionTimeout, InkEdit.put_RecognitionTimeout, RecognitionTimeout property [Tablet PC], RecognitionTimeout property [Tablet PC],IInkEdit interface, e1171aa3-841f-433e-88b8-e3fc63129aeb, get_RecognitionTimeout, inked/IInkEdit::RecognitionTimeout, inked/IInkEdit::get_RecognitionTimeout, inked/IInkEdit::put_RecognitionTimeout, put_RecognitionTimeout, tablet.inkedit_recotimeout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: inked.h
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
req.typenames: SelAlignmentConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkEd.dll
-	InkEd.dll.dll
api_name:
-	IInkEdit.RecognitionTimeout
-	IInkEdit.get_RecognitionTimeout
-	IInkEdit.put_RecognitionTimeout
-	InkEdit.get_RecognitionTimeout
-	InkEdit.put_RecognitionTimeout
product: Windows
targetos: Windows
req.lib: InkEd.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkEdit::get_RecognitionTimeout


## -description



Gets or sets the length of time, in milliseconds, between the last <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object collected and the beginning of text recognition.



This property is read/write.


## -parameters


## -remarks



Setting this property equal to zero prevents the ink from being replaced by the recognized text.




## -see-also




<a href="tablet.iinkedit_">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

