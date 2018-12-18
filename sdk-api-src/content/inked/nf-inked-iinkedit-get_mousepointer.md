---
UID: NF:inked.IInkEdit.get_MousePointer
title: IInkEdit::get_MousePointer
author: windows-sdk-content
description: Gets or sets a value indicating the type of mouse pointer to be displayed.
old-location: tablet\inkedit_mousepointer.htm
tech.root: tablet
ms.assetid: a5d9a6cc-d777-4619-b28b-17cc79584171
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInkEdit interface [Tablet PC],MousePointer property, IInkEdit.MousePointer, IInkEdit.get_MousePointer, IInkEdit::MousePointer, IInkEdit::get_MousePointer, IInkEdit::put_MousePointer, InkEdit.get_MousePointer, InkEdit.put_MousePointer, MousePointer property [Tablet PC], MousePointer property [Tablet PC],IInkEdit interface, get_MousePointer, inked/IInkEdit::MousePointer, inked/IInkEdit::get_MousePointer, inked/IInkEdit::put_MousePointer, put_MousePointer, tablet.inkedit_mousepointer
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
 - IInkEdit.MousePointer
 - IInkEdit.get_MousePointer
 - IInkEdit.put_MousePointer
 - InkEdit.get_MousePointer
 - InkEdit.put_MousePointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkEdit::get_MousePointer


## -description


Gets or sets a value indicating the type of mouse pointer to be displayed.

This property is read/write.


## -parameters


## -remarks



If you set the <b>MousePointer</b> property to <a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">IMP_Default</a>, the mouse cursor setting is based on the current cursor's drawing attributes. If the ink collector is disabled, the mouse cursor setting is based on the underlying windows mouse cursor <a href="https://msdn.microsoft.com/8f5f00a2-abe1-487e-a067-2b6d929824c7">DrawingAttributes</a> property. If the <b>MousePointer</b> property is set to <b>IMP_Custom</b> and the <a href="https://msdn.microsoft.com/11e7cf2d-e671-471f-9a13-1f55b62b4dfa">MouseIcon</a> property is <b>NULL</b>, then the ink collector no longer handles mouse cursor settings. Setting the mouse cursor to any other setting (other than the <b>MousePointer</b> property set to <b>IMP_Default</b> and the <b>MouseIcon</b> property set to <b>NULL</b>) forces the mouse cursor to use the current setting.

You can use this property when you want to indicate changes in functionality as the mouse pointer passes over controls on a form or dialog box. The <a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">IMP_Hourglass</a> setting is useful for indicating that the user should wait for a process or operation to finish.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

