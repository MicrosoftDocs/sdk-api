---
UID: NL:gdiplusimaging.ImageItemData
title: ImageItemData (gdiplusimaging.h)
description: The ImageItemData class is used to store and retrieve custom image metadata. Windows GDI+ supports custom metadata for JPEG, PNG, and GIF image files.
helpviewer_keywords: ["ImageItemData","ImageItemData class [GDI+]","ImageItemData class [GDI+]","described","_gdiplus_CLASS_ImageItemData_Class","gdiplus._gdiplus_CLASS_ImageItemData_Class","gdiplusimaging/ImageItemData"]
old-location: gdiplus\_gdiplus_CLASS_ImageItemData_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageitemdata.htm
ms.date: 12/05/2018
ms.keywords: ImageItemData, ImageItemData class [GDI+], ImageItemData class [GDI+],described, _gdiplus_CLASS_ImageItemData_Class, gdiplus._gdiplus_CLASS_ImageItemData_Class, gdiplusimaging/ImageItemData
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - ImageItemData
 - gdiplusimaging/ImageItemData
dev_langs:
 - c++
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
---

# ImageItemData class


## -description

The <b>ImageItemData</b> class is used to store and retrieve custom image metadata. Windows GDI+ supports custom metadata for JPEG, PNG, and GIF image files.

<b>ImageItemData</b> has these types of members:

## -remarks

To retrieve custom metadata from an image file, call <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getitemdata">Image::GetItemData</a>. To store custom metadata in an image file, follow these steps:

		    

<ol>
<li>Create and initialize an <b>ImageItemData</b> object.</li>
<li>Create an <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object that has an array of one or more <a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a> objects.</li>
<li>For one of the <a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a> objects in the array, set the Value member to the address of your <b>ImageItemData</b> object. Set the other members as follows: Guid = EncoderImageItems, Type = EncoderParameterValueTypePointer,  NumberOfValues = 1.</li>
<li>Pass the address of the <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object to the <a href="/previous-versions/ms535407(v=vs.85)">Image::Save</a> method of an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.</li>
</ol>

#### Examples



The following example saves a piece of custom metadata in a JPEG file. The code relies on a helper function, GetEncoderClsid, to get the class identifier for the JPEG encoder. To see the source code for GetEncoderClsid, see <a href="/windows/desktop/gdiplus/-gdiplus-retrieving-the-class-identifier-for-an-encoder-use">Retrieving the Class Identifier for an Encoder</a>.


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