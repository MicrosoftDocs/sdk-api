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

# CachedBitmap::CachedBitmap(IN Bitmap,IN Graphics)


## -description


Creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object and a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. The cached bitmap takes the pixel data from the <b>Bitmap</b> object and stores it in a format that is optimized for the display device associated with the <b>Graphics</b> object.


## -parameters




#### - bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object that contains the pixel data to be optimized. 


#### - graphics [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object that is associated with a display device for which the image will be optimized. 


## -remarks



You can display a cached bitmap by passing the address of a <b>CachedBitmap::CachedBitmap</b> object to the 
				<a href="https://msdn.microsoft.com/9b7a2015-7d10-4b7a-88f4-c3b4d92c888d">DrawCachedBitmap</a> method of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. Use the <b>Graphics</b> object that was passed to the <b>CachedBitmap::CachedBitmap</b> constructor or another <b>Graphics</b> object that represents the same device.


#### Examples



The following example creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object and a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. The code calls the 
						<a href="https://msdn.microsoft.com/9b7a2015-7d10-4b7a-88f4-c3b4d92c888d">DrawCachedBitmap</a> method of that <b>Graphics</b> object to display the cached bitmap.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_CachedBitmap(HDC hdc)
{
   Graphics graphics(hdc);
   Bitmap bitmap(L"Grapes.jpg");
   CachedBitmap cachedBitmap(&amp;bitmap, &amp;graphics);

   graphics.DrawCachedBitmap(&amp;cachedBitmap, 10, 10);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/42e2b664-197c-4c54-9220-b6231d6439d0">Using a Cached Bitmap to Improve Performance</a>
 

 

