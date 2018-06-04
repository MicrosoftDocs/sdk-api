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

# ITextDocument2::GetEffectColor


## -description


Retrieves the color used for special text attributes.


## -parameters




### -param Index [in]

Type: <b>long</b>

The index of the color to retrieve. It can be one of the following values.

<table>
<tr>
<th>Index</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Text color.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
RGB(0,   0,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
RGB(0,   0, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
RGB(0, 255, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
RGB(0, 255,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
RGB(255,   0, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
RGB(255,   0, 0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
RGB(255,   255, 0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>8</dt>
</dl>
</td>
<td width="60%">
RGB(255,   255, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>9</dt>
</dl>
</td>
<td width="60%">
RGB(0,   0, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
RGB(0,   128, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
RGB(0, 128,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>12</dt>
</dl>
</td>
<td width="60%">
RGB(128,   0, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>13</dt>
</dl>
</td>
<td width="60%">
RGB(128,   0,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>14</dt>
</dl>
</td>
<td width="60%">
RGB(128, 128,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>15</dt>
</dl>
</td>
<td width="60%">
RGB(128, 128, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>16</dt>
</dl>
</td>
<td width="60%">
RGB(192, 192, 192)

</td>
</tr>
</table>
 


### -param pValue [out]

Type: <b>long*</b>

The color that corresponds to the specified index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The first 16 index values are for special underline colors. If an index between 1 and 16 hasn't been defined by a call to the <a href="https://msdn.microsoft.com/6371b525-96da-42a7-8cee-228b47208f46">ITextDocument2:SetEffectColor</a> method, <b>GetEffectColor</b> returns the corresponding Microsoft Word default color. 




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/6371b525-96da-42a7-8cee-228b47208f46">ITextDocument2::SetEffectColor</a>
 

 

