---
UID: NF:inked.IInkEdit.put_SelFontName
title: IInkEdit::put_SelFontName
author: windows-sdk-content
description: Gets or sets the font name of the selected text within the InkEdit control (run time only).
old-location: tablet\inkedit_selfontname.htm
tech.root: tablet
ms.assetid: 2aa1e53b-75cc-412d-b522-2e1c91ce31d3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IInkEdit interface [Tablet PC],SelFontName property, IInkEdit.SelFontName, IInkEdit.put_SelFontName, IInkEdit::SelFontName, IInkEdit::get_SelFontName, IInkEdit::put_SelFontName, InkEdit.get_SelFontName, InkEdit.put_SelFontName, SelFontName property [Tablet PC], SelFontName property [Tablet PC],IInkEdit interface, get_SelFontName, inked/IInkEdit::SelFontName, inked/IInkEdit::get_SelFontName, inked/IInkEdit::put_SelFontName, put_SelFontName, tablet.inkedit_selfontname
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IInkEdit::put_SelFontName


## -description


Gets or sets the font name of the selected text within the InkEdit control (run time only).

This property is read/write.


## -parameters


## -remarks



If a selection spans multiple characters with different fonts, the <a href="https://msdn.microsoft.com/06a4ed72-e2c2-4422-8796-39a65b19415e">SelColor</a> property will be <b>NULL</b>.

If there is no text selected in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control, setting this property determines the font of all new text entered at the current insertion point.




## -see-also




<a href="https://msdn.microsoft.com/8F47529B-52E9-4D67-81B3-DD2584B98101">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

