---
UID: NF:inked.IInkEdit.get_SelText
title: IInkEdit::get_SelText (inked.h)

description: Gets or sets the selected text within the InkEdit control (run time only).
old-location: tablet\inkedit_seltext.htm
tech.root: tablet
ms.assetid: 2cd805b5-f421-48d1-9678-b3cae0bc6b86

ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelText property, IInkEdit.SelText, IInkEdit.get_SelText, IInkEdit::SelText, IInkEdit::get_SelText, IInkEdit::put_SelText, InkEdit.get_SelText, InkEdit.put_SelText, SelText property [Tablet PC], SelText property [Tablet PC],IInkEdit interface, get_SelText, inked/IInkEdit::SelText, inked/IInkEdit::get_SelText, inked/IInkEdit::put_SelText, put_SelText, tablet.inkedit_seltext
ms.topic: method
f1_keywords: 
 - "inked/IInkEdit.SelText"
dev_langs:
 - c++
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
 - IInkEdit.SelText
 - IInkEdit.get_SelText
 - IInkEdit.put_SelText
 - InkEdit.get_SelText
 - InkEdit.put_SelText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::get_SelText


## -description


Gets or sets the selected text within the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

This property is read/write.


## -parameters


## -remarks



Setting <b>SelText</b> to a new value sets <a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength">SelLength</a> to 0 and replaces the selected text with the new string. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

