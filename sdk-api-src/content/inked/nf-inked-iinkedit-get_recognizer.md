---
UID: NF:inked.IInkEdit.get_Recognizer
title: IInkEdit::get_Recognizer
author: windows-sdk-content
description: Gets or sets the IInkRecognizer object to use for recognition.
old-location: tablet\inkedit_recognizer.htm
old-project: tablet
ms.assetid: 531bc7f0-1a62-40c2-81f9-ceafe9388a0e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 531bc7f0-1a62-40c2-81f9-ceafe9388a0e, IInkEdit interface [Tablet PC],Recognizer property, IInkEdit.Recognizer, IInkEdit.get_Recognizer, IInkEdit::Recognizer, IInkEdit::get_Recognizer, IInkEdit::put_Recognizer, InkEdit.get_Recognizer, InkEdit.putref_Recognizer, Recognizer property [Tablet PC], Recognizer property [Tablet PC],IInkEdit interface, get_Recognizer, inked/IInkEdit::Recognizer, inked/IInkEdit::get_Recognizer, inked/IInkEdit::put_Recognizer, putref_Recognizer, tablet.inkedit_recognizer
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
tech.root: 
req.typenames: SelAlignmentConstants
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
req.lib: InkEd.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkEdit::get_Recognizer


## -description



Gets or sets the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object to use for recognition.



This property is read/write.


## -parameters


## -remarks



This property is run time only.

This property should only be changed if the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property returns IES_Idle.

If a factoid is used for the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, it must be reapplied after setting this property.




## -see-also




<a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid Constants</a>



<a href="/windows/desktop/api/inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

