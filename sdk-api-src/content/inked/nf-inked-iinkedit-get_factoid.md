---
UID: NF:inked.IInkEdit.get_Factoid
title: IInkEdit::get_Factoid
author: windows-sdk-content
description: Gets or sets the Factoid constant that a IInkRecognizer object uses to constrain its search for the recognition result.
old-location: tablet\inkedit_factoid.htm
old-project: tablet
ms.assetid: 150325e4-dd8b-4abf-baa6-f0fda05d2fd9
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: 150325e4-dd8b-4abf-baa6-f0fda05d2fd9, Factoid property [Tablet PC], Factoid property [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],Factoid property, IInkEdit.Factoid, IInkEdit.get_Factoid, IInkEdit::Factoid, IInkEdit::get_Factoid, IInkEdit::put_Factoid, InkEdit.get_Factoid, InkEdit.put_Factoid, get_Factoid, inked/IInkEdit::Factoid, inked/IInkEdit::get_Factoid, inked/IInkEdit::put_Factoid, put_Factoid, tablet.inkedit_factoid
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
 - IInkEdit.Factoid
 - IInkEdit.get_Factoid
 - IInkEdit.put_Factoid
 - InkEdit.get_Factoid
 - InkEdit.put_Factoid
product: Windows
targetos: Windows
req.lib: InkEd.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkEdit::get_Factoid


## -description



Gets or sets the <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid</a> constant that a <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object uses to constrain its search for the recognition result.



This property is read/write.


## -parameters


## -remarks



This property should only be changed if the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property returns IES_Idle.

To ensure that ink is recognized in the correct field context, set this property before processing the ink for the first time.

A <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid</a> provides context for recognized ink in the context of a particular field. You specify a factoid if an input field is of a known type, for example, if the input field contains a date.

This property takes or returns a string parameter and not a class object of the <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid</a> class. The members of this class are of type STRING. This method does not throw an error if you attempt to set this property to an invalid string value.

<div class="alert"><b>Note</b>  All factoids are case sensitive.</div>
<div> </div>
For more information about factoids and how to use them, see <a href="https://msdn.microsoft.com/b64f6856-453c-4080-84e0-0a9e69e79de7">Using Context to Improve Accuracy</a>. For a list of supported factoids, see <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid Constants</a> and <a href="https://msdn.microsoft.com/9d5fc370-ba58-438b-8850-f31f0f0f6608">Supported Factoids from Version 1</a>.




## -see-also




<a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid Constants</a>



<a href="https://msdn.microsoft.com/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

