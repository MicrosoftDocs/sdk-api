---
UID: NF:tom.ITextRange.IsEqual
title: ITextRange::IsEqual
author: windows-sdk-content
description: Determines whether this range has the same character positions and story as those of a specified range.
old-location: controls\ITextRange_IsEqual.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextrange\itextrangeisequal.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextRange interface [Windows Controls],IsEqual method, ITextRange.IsEqual, ITextRange::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextRange interface, _win32_ITextRange_IsEqual, _win32_ITextRange_IsEqual_cpp, controls.ITextRange_IsEqual, controls._win32_ITextRange_IsEqual, tom/ITextRange::IsEqual
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.IsEqual
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::IsEqual


## -description


Determines whether this range has the same character positions and story as those of a specified range. 


## -parameters




### -param pRange

Type: <b><a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>*</b>

The <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> object that is compared to this range. 


### -param pValue






#### - pB

Type: <b>long*</b>

The comparison result. The pointer can be null. The <i>pB</i> parameter receives <b>tomTrue</b> if this range points at the same text (has the same start and end character positions and story) as <i>pRange</i>; otherwise it returns <b>tomFalse</b>. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the ranges have the same character positions and story, the method returns <b>S_OK</b>. Otherwise, it returns S_FALSE.




## -remarks



The 
				<b>ITextRange::IsEqual</b> method returns <b>tomTrue</b> only if the range points at the same text as <i>pRange</i>. See <a href="About_Text_Object_Model.htm">Finding Rich Text</a> for code that compares two different pieces of text to see if they contain the same plain text and the same character formatting.




## -see-also




<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

