---
UID: NF:inked.IInkEdit.get_SelFontName
title: IInkEdit::get_SelFontName (inked.h)
author: windows-sdk-content
description: Gets or sets the font name of the selected text within the InkEdit control (run time only).
old-location: tablet\inkedit_selfontname.htm
tech.root: tablet
ms.assetid: 2aa1e53b-75cc-412d-b522-2e1c91ce31d3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelFontName property, IInkEdit.SelFontName, IInkEdit.get_SelFontName, IInkEdit::SelFontName, IInkEdit::get_SelFontName, IInkEdit::put_SelFontName, InkEdit.get_SelFontName, InkEdit.put_SelFontName, SelFontName property [Tablet PC], SelFontName property [Tablet PC],IInkEdit interface, get_SelFontName, inked/IInkEdit::SelFontName, inked/IInkEdit::get_SelFontName, inked/IInkEdit::put_SelFontName, put_SelFontName, tablet.inkedit_selfontname
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
 - IInkEdit.SelFontName
 - IInkEdit.get_SelFontName
 - IInkEdit.put_SelFontName
 - InkEdit.get_SelFontName
 - InkEdit.put_SelFontName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::get_SelFontName


## -description


Gets or sets the font name of the selected text within the InkEdit control (run time only).

This property is read/write.


## -parameters


## -remarks



If a selection spans multiple characters with different fonts, the <a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor">SelColor</a> property will be <b>NULL</b>.

If there is no text selected in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control, setting this property determines the font of all new text entered at the current insertion point.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

