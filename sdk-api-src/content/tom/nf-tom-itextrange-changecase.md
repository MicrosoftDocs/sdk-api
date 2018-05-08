---
UID: NF:tom.ITextRange.ChangeCase
title: ITextRange::ChangeCase
author: windows-driver-content
description: Changes the case of letters in this range according to the Type parameter.
old-location: controls\ITextRange_ChangeCase.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\changecase.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ChangeCase, ChangeCase method [Windows Controls], ChangeCase method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],ChangeCase method, ITextRange.ChangeCase, ITextRange::ChangeCase, _win32_ITextRange_ChangeCase, _win32_ITextRange_ChangeCase_cpp, controls.ITextRange_ChangeCase, controls._win32_ITextRange_ChangeCase, tom/ITextRange::ChangeCase, tomLowerCase, tomSentenceCase, tomTitleCase, tomToggleCase, tomUpperCase
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRange.ChangeCase
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::ChangeCase


## -description


Changes the case of letters in this range according to the 
			<i>Type</i> parameter.


## -parameters




### -param Type [in]

Type: <b>long</b>

Type of case change. The default value is <i>tomLower</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomLowerCase"></a><a id="tomlowercase"></a><a id="TOMLOWERCASE"></a><dl>
<dt><b>tomLowerCase</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">

							Sets all text to lowercase.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomUpperCase"></a><a id="tomuppercase"></a><a id="TOMUPPERCASE"></a><dl>
<dt><b>tomUpperCase</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">

							Sets all text to lowercase.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomTitleCase"></a><a id="tomtitlecase"></a><a id="TOMTITLECASE"></a><dl>
<dt><b>tomTitleCase</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">

							Capitalizes the first letter of each word.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomSentenceCase"></a><a id="tomsentencecase"></a><a id="TOMSENTENCECASE"></a><dl>
<dt><b>tomSentenceCase</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">

							Capitalizes the first letter of each sentence.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomToggleCase"></a><a id="tomtogglecase"></a><a id="TOMTOGGLECASE"></a><dl>
<dt><b>tomToggleCase</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">

							Toggles the case of each letter.
						

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

This method returns an 
						<b>HRESULT</b> value. If successful, it returns <b>S_OK</b>. Otherwise, it returns S_FALSE. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

