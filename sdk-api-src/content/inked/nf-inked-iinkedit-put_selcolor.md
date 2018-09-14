---
UID: NF:inked.IInkEdit.put_SelColor
title: IInkEdit::put_SelColor
author: windows-sdk-content
description: Gets or sets the text color of the current text selection or insertion point (run time only).
old-location: tablet\inkedit_selcolor.htm
tech.root: tablet
ms.assetid: 06a4ed72-e2c2-4422-8796-39a65b19415e
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IInkEdit interface [Tablet PC],SelColor property, IInkEdit.SelColor, IInkEdit.put_SelColor, IInkEdit::SelColor, IInkEdit::get_SelColor, IInkEdit::put_SelColor, InkEdit.get_SelColor, InkEdit.put_SelColor, SelColor property [Tablet PC], SelColor property [Tablet PC],IInkEdit interface, get_SelColor, inked/IInkEdit::SelColor, inked/IInkEdit::get_SelColor, inked/IInkEdit::put_SelColor, put_SelColor, tablet.inkedit_selcolor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inked.h
api_name:
 - IInkEdit.SelColor
 - IInkEdit.get_SelColor
 - IInkEdit.put_SelColor
 - InkEdit.get_SelColor
 - InkEdit.put_SelColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkEdit::put_SelColor


## -description


Gets or sets the text color of the current text selection or insertion point (run time only).

This property is read/write.


## -parameters


## -remarks



If a selection spans multiple characters with different colors, the <b>SelColor</b> property will be <b>NULL</b>.

If there is no text selected in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control, setting this property determines the color of all new text entered at the current insertion point.




## -see-also




<a href="https://msdn.microsoft.com/8F47529B-52E9-4D67-81B3-DD2584B98101">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

