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
 

 

