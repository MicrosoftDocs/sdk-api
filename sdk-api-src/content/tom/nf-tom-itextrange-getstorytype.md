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

# ITextRange::GetStoryType


## -description


Get the type of the range's story.


## -parameters




### -param pValue

Type: <b>long*</b>

The type of the range's story. The <i>pValue</i> value can be one of the following values. 
					

<table class="clsStd">
<tr>
<th>Story type</th>
<th>Value</th>
<th>Story type</th>
<th>Value</th>
</tr>
<tr>
<td><b>tomUnknownStory</b></td>
<td>0</td>
<td><b>tomEvenPagesHeaderStory</b></td>
<td>6</td>
</tr>
<tr>
<td><b>tomMainTextStory</b></td>
<td>1</td>
<td><b>tomPrimaryHeaderStory</b></td>
<td>7</td>
</tr>
<tr>
<td><b>tomFootnotesStory</b></td>
<td>2</td>
<td><b>tomEvenPagesFooterStory</b></td>
<td>8</td>
</tr>
<tr>
<td><b>tomEndnotesStory</b></td>
<td>3</td>
<td><b>tomPrimaryFooterStory</b></td>
<td>9</td>
</tr>
<tr>
<td><b>tomCommentsStory</b></td>
<td>4</td>
<td><b>tomFirstPageHeaderStory</b></td>
<td>10</td>
</tr>
<tr>
<td><b>tomTextFrameStory</b></td>
<td>5</td>
<td><b>tomFirstPageFooterStory</b></td>
<td>11</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pValue</i> is null, the method fails and it returns E_INVALIDARG.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

