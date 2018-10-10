---
UID: NF:gdiplusheaders.Image.FindNextItem
title: Image::FindNextItem
author: windows-sdk-content
description: The Image::FindNextItem method is used along with the Image::FindFirstItem method to enumerate the metadata items stored in this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_FindNextItem_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\findnextitem.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FindNextItem, FindNextItem method [GDI+], FindNextItem method [GDI+],Image class, Image class [GDI+],FindNextItem method, Image.FindNextItem, Image::FindNextItem, _gdiplus_CLASS_Image_FindNextItem_, gdiplus._gdiplus_CLASS_Image_FindNextItem_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.FindNextItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Image::FindNextItem


## -description


The <b>Image::FindNextItem</b> method is used along with the <a href="https://msdn.microsoft.com/7689f6b9-3c0b-4083-aed9-0ce3ab2accaa">Image::FindFirstItem</a> method to enumerate the metadata items stored in this <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. The <b>Image::FindNextItem</b> method retrieves the description and the data size of the next metadata item in this <b>Image</b> object. 


## -parameters




### -param item [in, out]

Type: <b><a href="https://msdn.microsoft.com/56316228-9cae-46d5-bfef-bbd523aabd2b">ImageItemData</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/56316228-9cae-46d5-bfef-bbd523aabd2b">ImageItemData</a> object. On input, the Desc member points to a buffer (allocated by the caller) large enough to hold the metadata description (1 byte for JPEG, 4 bytes for PNG, 11 bytes for GIF), and the DescSize member specifies the size (1, 4, or 6) of the buffer pointed to by Desc. On output, the buffer pointed to by Desc receives the metadata description, and the DataSize member receives the size, in bytes, of the metadata itself.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks




<a href="https://msdn.microsoft.com/7689f6b9-3c0b-4083-aed9-0ce3ab2accaa">Image::FindFirstItem</a> and <b>Image::FindNextItem</b> do not enumerate the metadata items stored by the <a href="https://msdn.microsoft.com/20201f1e-fa80-4a7b-b7cc-7737d4a434a5">Image::SetPropertyItem</a> method.


#### Examples



The following example displays the description and data size for each metadata item in an Image object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Status stat;        
Image image(L"River5.png");

CHAR descBuf[5] = {0, 0, 0, 0, 0};
ImageItemData itemData;
ZeroMemory(&amp;itemData, sizeof(itemData));
itemData.Size = sizeof(itemData);
itemData.DescSize = 4;
itemData.Desc = descBuf;

stat = image.FindFirstItem(&amp;itemData);

while(Ok == stat)
{
   printf("%s   %d\n", itemData.Desc, itemData.DataSize);
   stat = image.FindNextItem(&amp;itemData);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/cbda0682-7b06-4a7a-92ec-ef5c181a23bb">Image::GetItemData</a>
 

 

