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



This method differs from <a href="https://msdn.microsoft.com/e6de647e-c3db-4038-8d7e-4b36fdbf3577">ITextRange::GetChar</a> in the following ways:<ul>
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
 

 

