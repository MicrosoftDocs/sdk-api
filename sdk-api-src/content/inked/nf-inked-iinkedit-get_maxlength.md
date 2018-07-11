---
UID: NF:inked.IInkEdit.get_MaxLength
title: IInkEdit::get_MaxLength
author: windows-sdk-content
description: Gets or sets a value indicating whether there is a maximum number of characters an InkEdit control can hold and, if so, specifies the maximum number of characters.
old-location: tablet\inkedit_maxlength.htm
old-project: tablet
ms.assetid: 603074d4-3222-4593-a5e8-b5f8a8dced6a
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IInkEdit interface [Tablet PC],MaxLength property, IInkEdit.MaxLength, IInkEdit.get_MaxLength, IInkEdit::MaxLength, IInkEdit::get_MaxLength, IInkEdit::put_MaxLength, InkEdit.get_MaxLength, InkEdit.put_MaxLength, MaxLength property [Tablet PC], MaxLength property [Tablet PC],IInkEdit interface, get_MaxLength, inked/IInkEdit::MaxLength, inked/IInkEdit::get_MaxLength, inked/IInkEdit::put_MaxLength, put_MaxLength, tablet.inkedit_maxlength
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
 - IInkEdit.MaxLength
 - IInkEdit.get_MaxLength
 - IInkEdit.put_MaxLength
 - InkEdit.get_MaxLength
 - InkEdit.put_MaxLength
product: Windows
targetos: Windows
req.lib: InkEd.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkEdit::get_MaxLength


## -description


 Gets or sets a value indicating whether there is a maximum number of characters an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control can hold and, if so, specifies the maximum number of characters.


This property is read/write.


## -parameters


## -remarks



The default for the <b>MaxLength</b> property is 0, indicating no maximum other than that created by memory constraints on the user's system. Any number greater than 0 indicates the maximum number of characters.

Use the <b>MaxLength</b> property to limit the number of characters a user can enter in an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.



If text that exceeds the <b>MaxLength</b> property setting is assigned to an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control from code, no error occurs; however, only the maximum number of characters is assigned to the <a href="https://msdn.microsoft.com/library/Dd374074(v=VS.85).aspx">Text</a> property, and extra characters are truncated. Changing this property doesn't affect the current contents of an InkEdit control, but will affect any subsequent changes to the contents.






## -see-also




<a href="https://msdn.microsoft.com/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

