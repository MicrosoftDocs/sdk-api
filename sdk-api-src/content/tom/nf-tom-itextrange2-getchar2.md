---
UID: NF:tom.ITextRange2.GetChar2
title: ITextRange2::GetChar2
author: windows-sdk-content
description: Gets the character at the specified offset from the end of this range.
old-location: controls\itextrange2_getchar2.htm
tech.root: Controls
ms.assetid: 8ece8ca0-fd05-481c-9ce2-b2b7a3df354e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetChar2, GetChar2 method [Windows Controls], GetChar2 method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetChar2 method, ITextRange2.GetChar2, ITextRange2::GetChar2, controls.itextrange2_getchar2, tom/ITextRange2::GetChar2
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
 - ITextRange2.GetChar2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::GetChar2


## -description


Gets the character at the specified offset from the end of this range. 


## -parameters




### -param pChar [out]

Type: <b>long*</b>

The character value.


### -param Offset [in]

Type: <b>long</b>

The offset from the end of the range. An offset of 0 gets the character at the end of the range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method differs from <a href="https://msdn.microsoft.com/en-us/library/Bb773937(v=VS.85).aspx">ITextRange::GetChar</a> in the following ways:<ul>
<li>It returns the UTF-32 character for the surrogate pair instead of the pair's lead code.</li>
<li>It gets the character code, or codes, at the specified offset from the end of the range instead of the character at the start of the range. </li>
</ul>


If the character is the lead code for a surrogate pair, the corresponding UTF-32 character is returned. 

If <i>Offset</i> specifies a character before the start of the story or at the end of the story, this method returns the character code 0. 


<table>
<tr>
<th>If the Offset value is</th>
<th>This character is returned</th>
</tr>
<tr>
<td>0</td>
<td>The character at the end of the range.</td>
</tr>
<tr>
<td>Negative and accesses the middle of a surrogate pair</td>
<td>The corresponding UTF-32 character.</td>
</tr>
<tr>
<td>Positive and accesses the middle of a surrogate pair</td>
<td>The UTF-32 character following that pair.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

