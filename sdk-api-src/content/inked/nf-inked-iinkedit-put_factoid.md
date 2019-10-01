---
UID: NF:inked.IInkEdit.put_Factoid
title: IInkEdit::put_Factoid (inked.h)
author: windows-sdk-content
description: Gets or sets the Factoid constant that a IInkRecognizer object uses to constrain its search for the recognition result.
old-location: tablet\inkedit_factoid.htm
tech.root: tablet
ms.assetid: 150325e4-dd8b-4abf-baa6-f0fda05d2fd9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 150325e4-dd8b-4abf-baa6-f0fda05d2fd9, Factoid property [Tablet PC], Factoid property [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],Factoid property, IInkEdit.Factoid, IInkEdit.put_Factoid, IInkEdit::Factoid, IInkEdit::get_Factoid, IInkEdit::put_Factoid, InkEdit.get_Factoid, InkEdit.put_Factoid, get_Factoid, inked/IInkEdit::Factoid, inked/IInkEdit::get_Factoid, inked/IInkEdit::put_Factoid, put_Factoid, tablet.inkedit_factoid
ms.topic: method
f1_keywords: 
 - "inked/IInkEdit.Factoid"
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
 - IInkEdit.Factoid
 - IInkEdit.get_Factoid
 - IInkEdit.put_Factoid
 - InkEdit.get_Factoid
 - InkEdit.put_Factoid
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::put_Factoid


## -description



Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/factoid-constants">Factoid</a> constant that a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object uses to constrain its search for the recognition result.



This property is read/write.


## -parameters


## -remarks



This property should only be changed if the <a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a> property returns IES_Idle.

To ensure that ink is recognized in the correct field context, set this property before processing the ink for the first time.

A <a href="https://docs.microsoft.com/windows/desktop/tablet/factoid-constants">Factoid</a> provides context for recognized ink in the context of a particular field. You specify a factoid if an input field is of a known type, for example, if the input field contains a date.

This property takes or returns a string parameter and not a class object of the <a href="https://docs.microsoft.com/windows/desktop/tablet/factoid-constants">Factoid</a> class. The members of this class are of type STRING. This method does not throw an error if you attempt to set this property to an invalid string value.

<div class="alert"><b>Note</b>  All factoids are case sensitive.</div>
<div> </div>
For more information about factoids and how to use them, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-context-to-improve-accuracy">Using Context to Improve Accuracy</a>. For a list of supported factoids, see <a href="https://docs.microsoft.com/windows/desktop/tablet/factoid-constants">Factoid Constants</a> and <a href="https://docs.microsoft.com/windows/desktop/tablet/supported-factoids-from-version-1">Supported Factoids from Version 1</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/factoid-constants">Factoid Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

