---
UID: NF:tom.ITextPara2.GetTrimPunctuationAtStart
title: ITextPara2::GetTrimPunctuationAtStart
author: windows-sdk-content
description: Gets whether to trim the leading space of a punctuation symbol at the start of a line.
old-location: controls\itextpara2_gettrimpunctuationatstart.htm
tech.root: Controls
ms.assetid: 965df0ef-b8ff-4d0e-8124-c811e74e0208
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetTrimPunctuationAtStart, GetTrimPunctuationAtStart method [Windows Controls], GetTrimPunctuationAtStart method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetTrimPunctuationAtStart method, ITextPara2.GetTrimPunctuationAtStart, ITextPara2::GetTrimPunctuationAtStart, controls.itextpara2_gettrimpunctuationatstart, tom/ITextPara2::GetTrimPunctuationAtStart
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITextPara2.GetTrimPunctuationAtStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara2::GetTrimPunctuationAtStart


## -description


Gets whether to trim the leading space of a punctuation symbol at the start of a line.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">tomBool</a> value that can be one of the following.

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
<td><b>tomUndefined</b></td>
<td>The TrimPunctuationAtStart property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/f08f67ca-5767-4986-8af1-b3a11a1065aa">ITextPara2::SetTrimPunctuationAtStart</a>
 

 

