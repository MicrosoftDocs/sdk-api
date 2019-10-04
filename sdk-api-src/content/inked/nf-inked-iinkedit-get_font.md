---
UID: NF:inked.IInkEdit.get_Font
title: IInkEdit::get_Font (inked.h)
author: windows-sdk-content
description: Gets or sets a Font object.
old-location: tablet\inkedit_font.htm
tech.root: tablet
ms.assetid: af8234bb-7d53-45c7-9edc-fd4e6b64eed3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Font property [Tablet PC], Font property [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],Font property, IInkEdit.Font, IInkEdit.get_Font, IInkEdit::Font, IInkEdit::get_Font, IInkEdit::put_Font, InkEdit.get_Font, InkEdit.putref_Font, get_Font, inked/IInkEdit::Font, inked/IInkEdit::get_Font, inked/IInkEdit::put_Font, putref_Font, tablet.inkedit_font
ms.topic: method
f1_keywords: 
 - "inked/IInkEdit.Font"
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
 - IInkEdit.Font
 - IInkEdit.get_Font
 - IInkEdit.put_Font
 - InkEdit.get_Font
 - InkEdit.putref_Font
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::get_Font


## -description


Gets or sets a Font object.

This property is read/write.


## -parameters


## -remarks



Use the <b>Font</b> property of an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control to identify a specific Font object whose properties you want to use. For example, the following code changes the <b>Bold</b> property setting of a Font object identified by the <b>Font</b> property of an InkEdit control:

<code>myInkEditControl.Font.Bold = true;</code>




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

