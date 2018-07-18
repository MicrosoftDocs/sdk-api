---
UID: NF:tom.ITextPara2.SetTrimPunctuationAtStart
title: ITextPara2::SetTrimPunctuationAtStart
author: windows-sdk-content
description: Sets whether to trim the leading space of a punctuation symbol at the start of a line.
old-location: controls\itextpara2_settrimpunctuationatstart.htm
old-project: controls
ms.assetid: f08f67ca-5767-4986-8af1-b3a11a1065aa
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetTrimPunctuationAtStart method, ITextPara2.SetTrimPunctuationAtStart, ITextPara2::SetTrimPunctuationAtStart, SetTrimPunctuationAtStart, SetTrimPunctuationAtStart method [Windows Controls], SetTrimPunctuationAtStart method [Windows Controls],ITextPara2 interface, controls.itextpara2_settrimpunctuationatstart, tom/ITextPara2::SetTrimPunctuationAtStart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextPara2.SetTrimPunctuationAtStart
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara2::SetTrimPunctuationAtStart


## -description


Sets whether to trim the leading space of a punctuation symbol at the start of a line.


## -parameters




### -param Value [in]

Type: <b>long</b>

A <a href="About_Text_Object_Model.htm">tomBool</a> that indicates whether to trim the leading space of a punctuation symbol. It can be one of the following values.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Trim the leading space of a punctuation symbol at the start of a line.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not trim the leading space of a punctuation symbol at the start of a line.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the TrimPunctuationAtStart property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The TrimPunctuationAtStart property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/965df0ef-b8ff-4d0e-8124-c811e74e0208">ITextPara2::GetTrimPunctuationAtStart</a>
 

 

