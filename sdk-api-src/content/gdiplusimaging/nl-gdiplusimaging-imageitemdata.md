---
UID: NL:gdiplusimaging.ImageItemData
title: ImageItemData
author: windows-driver-content
description: The ImageItemData class is used to store and retrieve custom image metadata. Windows GDI+ supports custom metadata for JPEG, PNG, and GIF image files.
old-location: gdiplus\_gdiplus_CLASS_ImageItemData_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageitemdata.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ImageItemData, ImageItemData class [GDI+], ImageItemData class [GDI+], described, _gdiplus_CLASS_ImageItemData_Class, gdiplus._gdiplus_CLASS_ImageItemData_Class, gdiplusimaging/ImageItemData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: gdiplusimaging.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.lib
-	Gdiplus.dll
api_name:
-	ImageItemData
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ImageItemData class


## -description


The <b>ImageItemData</b> class is used to store and retrieve custom image metadata. Windows GDI+ supports custom metadata for JPEG, PNG, and GIF image files.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">ImageItemData</b> has these types of members:


## -remarks



To retrieve custom metadata from an image file, call <a href="https://msdn.microsoft.com/cbda0682-7b06-4a7a-92ec-ef5c181a23bb">Image::GetItemData</a>. To store custom metadata in an image file, follow these steps:

		    

<ol>
<li>Create and initialize an <b>ImageItemData</b> object.</li>
<li>Create an <a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a> object that has an array of one or more <a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a> objects.</li>
<li>For one of the <a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a> objects in the array, set the Value member to the address of your <b>ImageItemData</b> object. Set the other members as follows: Guid = EncoderImageItems, Type = EncoderParameterValueTypePointer,  NumberOfValues = 1.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a> object to the <a href="https://msdn.microsoft.com/e2c57259-fe82-40dc-86a3-3f4110e6c0ee">Image::Save</a> method of an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.</li>
</ol>

#### Examples




			The following example saves a piece of custom metadata in a JPEG file. The code relies on a helper function, GetEncoderClsid, to get the class identifier for the JPEG encoder. To see the source code for GetEncoderClsid, see <a href="https://msdn.microsoft.com/f78dac7c-4bc1-4614-8a26-d99d5619399a">Retrieving the Class Identifier for an Encoder</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHAR myData[] = "Byte sequence of your choice";
BYTE description = 0xE4;

ImageItemData itemData;
itemData.Size = sizeof(itemData);
itemData.DescSize = 1;
itemData.Desc = &amp;description;
itemData.DataSize = 28;
itemData.Data = (VOID*)myData;
itemData.Position = ItemDataPositionAfterHeader;

// Get the Clsid of the JPEG encoder.
CLSID encoderClsid;
GetEncoderClsid(L"image/jpeg", &amp;encoderClsid);

EncoderParameters encoderParameters;
encoderParameters.Count = 1;
encoderParameters.Parameter[0].Guid = EncoderImageItems;
encoderParameters.Parameter[0].Type = EncoderParameterValueTypePointer;
encoderParameters.Parameter[0].NumberOfValues = 1; 
encoderParameters.Parameter[0].Value = &amp;itemData;

Image image(L"River.jpg");
image.Save(L"River2.jpg", &amp;encoderClsid, &amp;encoderParameters);</pre>
</td>
</tr>
</table></span></div>


