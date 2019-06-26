---
UID: NF:inked.IInkEdit.get_Recognizer
title: IInkEdit::get_Recognizer (inked.h)
author: windows-sdk-content
description: Gets or sets the IInkRecognizer object to use for recognition.
old-location: tablet\inkedit_recognizer.htm
tech.root: tablet
ms.assetid: 531bc7f0-1a62-40c2-81f9-ceafe9388a0e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 531bc7f0-1a62-40c2-81f9-ceafe9388a0e, IInkEdit interface [Tablet PC],Recognizer property, IInkEdit.Recognizer, IInkEdit.get_Recognizer, IInkEdit::Recognizer, IInkEdit::get_Recognizer, IInkEdit::put_Recognizer, InkEdit.get_Recognizer, InkEdit.putref_Recognizer, Recognizer property [Tablet PC], Recognizer property [Tablet PC],IInkEdit interface, get_Recognizer, inked/IInkEdit::Recognizer, inked/IInkEdit::get_Recognizer, inked/IInkEdit::put_Recognizer, putref_Recognizer, tablet.inkedit_recognizer
ms.topic: method
f1_keywords: 
 - "inked/IInkEdit.Recognizer"
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
req.lib: InkEd.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.Recognizer
 - IInkEdit.get_Recognizer
 - IInkEdit.put_Recognizer
 - InkEdit.get_Recognizer
 - InkEdit.putref_Recognizer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::get_Recognizer


## -description



Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object to use for recognition.



This property is read/write.


## -parameters


## -remarks



This property is run time only.

This property should only be changed if the <a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a> property returns IES_Idle.

If a factoid is used for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, it must be reapplied after setting this property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/factoid-constants">Factoid Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

