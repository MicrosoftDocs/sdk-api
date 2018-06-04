---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

