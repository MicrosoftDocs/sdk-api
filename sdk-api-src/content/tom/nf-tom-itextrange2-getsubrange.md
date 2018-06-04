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

# ITextRange2::GetSubrange


## -description


Retrieves a subrange in a range.


## -parameters




### -param iSubrange [in]

Type: <b>long</b>

The subrange index.


### -param pcpFirst [out]

Type: <b>long*</b>

The character position for the start of the subrange.


### -param pcpLim [out]

Type: <b>long*</b>

The character position for the end of the subrange.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Subranges are selected as follows.<table>
<tr>
<th>iSubrange value</th>
<th>Subrange</th>
</tr>
<tr>
<td>Equals zero</td>
<td>Gets the current active subrange.</td>
</tr>
<tr>
<td>Greater than zero</td>
<td>Gets the subrange at the index specified by <i>iSubrange</i>, in the order in which the subranges were added. This requires extra calculation.</td>
</tr>
<tr>
<td>Less than zero</td>
<td>Gets the subrange at the index specified by <i>iSubrange</i>, in increasing character position order.</td>
</tr>
</table>
 



See <a href="https://msdn.microsoft.com/a1744e60-74b0-44a0-b470-6e89d328fa11">ITextRange2::GetCount</a> for the count of subranges not including the active subrange.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

