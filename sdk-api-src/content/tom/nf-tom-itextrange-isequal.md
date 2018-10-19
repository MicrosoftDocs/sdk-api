---
UID: NF:tom.ITextRange.IsEqual
title: ITextRange::IsEqual
author: windows-sdk-content
description: Determines whether this range has the same character positions and story as those of a specified range.
old-location: controls\ITextRange_IsEqual.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextrange\itextrangeisequal.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ITextRange interface [Windows Controls],IsEqual method, ITextRange.IsEqual, ITextRange::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextRange interface, _win32_ITextRange_IsEqual, _win32_ITextRange_IsEqual_cpp, controls.ITextRange_IsEqual, controls._win32_ITextRange_IsEqual, tom/ITextRange::IsEqual
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ITextRange::IsEqual


## -description


Determines whether this range has the same character positions and story as those of a specified range. 


## -parameters




### -param pRange

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>*</b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> object that is compared to this range. 


### -param pValue

TBD




#### - pB

Type: <b>long*</b>

The comparison result. The pointer can be null. The <i>pB</i> parameter receives <b>tomTrue</b> if this range points at the same text (has the same start and end character positions and story) as <i>pRange</i>; otherwise it returns <b>tomFalse</b>. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the ranges have the same character positions and story, the method returns <b>S_OK</b>. Otherwise, it returns S_FALSE.




## -remarks



The 
				<b>ITextRange::IsEqual</b> method returns <b>tomTrue</b> only if the range points at the same text as <i>pRange</i>. See <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">Finding Rich Text</a> for code that compares two different pieces of text to see if they contain the same plain text and the same character formatting.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

