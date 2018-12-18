---
UID: NF:gdiplusheaders.Image.GetItemData
title: Image::GetItemData
author: windows-sdk-content
description: The Image::GetItemData method gets one piece of metadata from this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetItemData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getitemdata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetItemData, GetItemData method [GDI+], GetItemData method [GDI+],Image class, Image class [GDI+],GetItemData method, Image.GetItemData, Image::GetItemData, _gdiplus_CLASS_Image_GetItemData_, gdiplus._gdiplus_CLASS_Image_GetItemData_
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
 - Image.GetItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Image::GetItemData


## -description


The <b>Image::GetItemData</b> method gets one piece of metadata from this <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object.


## -parameters




### -param item [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534468(v=VS.85).aspx">ImageItemData</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534468(v=VS.85).aspx">ImageItemData</a> object that specifies the item to be retrieved. The Data member of the <b>ImageItemData</b> object points to a buffer that receives the custom metadata. If the Data member is set to <b>NULL</b>, this method returns the size of the required buffer in the DataSize member of the ImageItemData object.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>
 

 

