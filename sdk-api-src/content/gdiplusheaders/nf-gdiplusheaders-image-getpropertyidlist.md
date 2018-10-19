---
UID: NF:gdiplusheaders.Image.GetPropertyIdList
title: Image::GetPropertyIdList
author: windows-sdk-content
description: The Image::GetPropertyIdList method gets a list of the property identifiers used in the metadata of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPropertyIdList_numOfProperty_list_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpropertyidlist.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetPropertyIdList, GetPropertyIdList method [GDI+], GetPropertyIdList method [GDI+],Image class, Image class [GDI+],GetPropertyIdList method, Image.GetPropertyIdList, Image::GetPropertyIdList, _gdiplus_CLASS_Image_GetPropertyIdList_numOfProperty_list_, gdiplus._gdiplus_CLASS_Image_GetPropertyIdList_numOfProperty_list_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Image.GetPropertyIdList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetPropertyIdList


## -description


The <b>Image::GetPropertyIdList</b> method gets a list of the property identifiers used in the metadata of this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param numOfProperty [in]

Type: <b>UINT</b>

Integer that specifies the number of elements in the 
					<i>list</i> array. Call the <a href="https://msdn.microsoft.com/fff3acf1-2a2f-46b6-af7e-02b7ef52bb40">Image::GetPropertyCount</a> method to determine this number. 


### -param list [out]

Type: <b>PROPID*</b>

Pointer to an array that receives the property identifiers. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The <b>Image::GetPropertyIdList</b> method returns an array of 
				<b>PROPID</b>s. Before you call <b>Image::GetPropertyIdList</b>, you must allocate a buffer large enough to receive that array. You can call the <a href="https://msdn.microsoft.com/fff3acf1-2a2f-46b6-af7e-02b7ef52bb40">Image::GetPropertyCount</a> method of an 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object to determine the size of the required buffer. The size of the buffer should be the return value of <b>Image::GetPropertyCount</b> multiplied by 
				<b>sizeof</b>(
				<b>PROPID</b>).


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a JPEG file. The code calls the <b>Image::GetPropertyIdList</b> method of that 
						<b>Image</b> object to find out what types of metadata are stored in the image.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;gdiplus.h&gt;
#include &lt;stdio.h&gt;
using namespace Gdiplus;

INT main()
{
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&amp;gdiplusToken, &amp;gdiplusStartupInput, NULL);

   UINT count = 0; 
   Image* image = new Image(L"FakePhoto.jpg");

   // How many types of metadata are in the image?
   count = image-&gt;GetPropertyCount();
   if(count == 0)
      return 0;

   // Allocate a buffer to receive an array of PROPIDs.
   PROPID* propIDs = new PROPID[count];

   image-&gt;GetPropertyIdList(count, propIDs);

   // List the retrieved IDs.
   for(UINT j = 0; j &lt; count; ++j)
      printf("%x\n", propIDs[j]);

   delete [] propIDs;
   delete image;   
  
   GdiplusShutdown(gdiplusToken);
   return 0;
}</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>320
10f
110
9003
829a
5090
5091</pre>
</td>
</tr>
</table></span></div>
The preceding output shows the hexadecimal value of each property identifier. You can look up those numbers in Gdiplusimaging.h and find out that they represent the following property tags.


<table class="clsStd">
<tr>
<th>Hexadecimal value</th>
<th>Property tag</th>
</tr>
<tr>
<td>0x0320</td>
<td>PropertyTagImageTitle</td>
</tr>
<tr>
<td>0x010f</td>
<td>PropertyTagEquipMake</td>
</tr>
<tr>
<td>0x0110</td>
<td>PropertyTagEquipModel</td>
</tr>
<tr>
<td>0x9003</td>
<td>PropertyTagExifDTOriginal</td>
</tr>
<tr>
<td>0x829a</td>
<td>PropertyTagExifExposureTime</td>
</tr>
<tr>
<td>0x5090</td>
<td>PropertyTagLuminanceTable</td>
</tr>
<tr>
<td>0x5091</td>
<td>PropertyTagChrominanceTable</td>
</tr>
</table>
 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/c22c2027-9552-4f35-ba44-755d872ceea7">Image::GetAllPropertyItems</a>



<a href="https://msdn.microsoft.com/fff3acf1-2a2f-46b6-af7e-02b7ef52bb40">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/ca96c4a3-058f-4ba4-a8be-2692ecd76710">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/574d3d5b-2440-4ab4-9d90-75282ea0f10d">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/ad849843-80e7-4773-96b0-f50dbdbfd61b">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/20201f1e-fa80-4a7b-b7cc-7737d4a434a5">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a>



<a href="https://msdn.microsoft.com/2febea35-3fea-4a2d-baaf-7a4f935fc81f">Reading and Writing Metadata</a>
 

 

