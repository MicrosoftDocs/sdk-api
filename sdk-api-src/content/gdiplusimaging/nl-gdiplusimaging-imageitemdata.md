---
UID: NL:gdiplusimaging.ImageItemData
title: ImageItemData (gdiplusimaging.h)
author: windows-sdk-content
description: The ImageItemData class is used to store and retrieve custom image metadata. Windows GDI+ supports custom metadata for JPEG, PNG, and GIF image files.
old-location: gdiplus\_gdiplus_CLASS_ImageItemData_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageitemdata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageItemData, ImageItemData class [GDI+], ImageItemData class [GDI+],described, _gdiplus_CLASS_ImageItemData_Class, gdiplus._gdiplus_CLASS_ImageItemData_Class, gdiplusimaging/ImageItemData
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
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - ImageItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# ImageItemData class


## -description


The <b>ImageItemData</b> class is used to store and retrieve custom image metadata. Windows GDI+ supports custom metadata for JPEG, PNG, and GIF image files.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">ImageItemData</b> has these types of members:


## -remarks



To retrieve custom metadata from an image file, call <a href="https://msdn.microsoft.com/en-us/library/ms535382(v=VS.85).aspx">Image::GetItemData</a>. To store custom metadata in an image file, follow these steps:

		    

<ol>
<li>Create and initialize an <b>ImageItemData</b> object.</li>
<li>Create an <a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a> object that has an array of one or more <a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a> objects.</li>
<li>For one of the <a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a> objects in the array, set the Value member to the address of your <b>ImageItemData</b> object. Set the other members as follows: Guid = EncoderImageItems, Type = EncoderParameterValueTypePointer,  NumberOfValues = 1.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a> object to the <a href="https://msdn.microsoft.com/en-us/library/ms535407(v=VS.85).aspx">Image::Save</a> method of an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object.</li>
</ol>

#### Examples



The following example saves a piece of custom metadata in a JPEG file. The code relies on a helper function, GetEncoderClsid, to get the class identifier for the JPEG encoder. To see the source code for GetEncoderClsid, see <a href="https://msdn.microsoft.com/en-us/library/ms533843(v=VS.85).aspx">Retrieving the Class Identifier for an Encoder</a>.


```cpp
CHAR myData[] = "Byte sequence of your choice";
BYTE description = 0xE4;

ImageItemData itemData;
itemData.Size = sizeof(itemData);
itemData.DescSize = 1;
itemData.Desc = &description;
itemData.DataSize = 28;
itemData.Data = (VOID*)myData;
itemData.Position = ItemDataPositionAfterHeader;

// Get the Clsid of the JPEG encoder.
CLSID encoderClsid;
GetEncoderClsid(L"image/jpeg", &encoderClsid);

EncoderParameters encoderParameters;
encoderParameters.Count = 1;
encoderParameters.Parameter[0].Guid = EncoderImageItems;
encoderParameters.Parameter[0].Type = EncoderParameterValueTypePointer;
encoderParameters.Parameter[0].NumberOfValues = 1; 
encoderParameters.Parameter[0].Value = &itemData;

Image image(L"River.jpg");
image.Save(L"River2.jpg", &encoderClsid, &encoderParameters);
```




