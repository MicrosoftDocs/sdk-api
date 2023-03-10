---
UID: NF:gdiplusheaders.Image.GetItemData
title: Image::GetItemData (gdiplusheaders.h)
description: The Image::GetItemData method gets one piece of metadata from this Image object.
helpviewer_keywords: ["GetItemData","GetItemData method [GDI+]","GetItemData method [GDI+]","Image class","Image class [GDI+]","GetItemData method","Image.GetItemData","Image::GetItemData","_gdiplus_CLASS_Image_GetItemData_","gdiplus._gdiplus_CLASS_Image_GetItemData_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetItemData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getitemdata.htm
ms.date: 12/05/2018
ms.keywords: GetItemData, GetItemData method [GDI+], GetItemData method [GDI+],Image class, Image class [GDI+],GetItemData method, Image.GetItemData, Image::GetItemData, _gdiplus_CLASS_Image_GetItemData_, gdiplus._gdiplus_CLASS_Image_GetItemData_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Image::GetItemData
 - gdiplusheaders/Image::GetItemData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.GetItemData
---

# Image::GetItemData


## -description

The <b>Image::GetItemData</b> method gets one piece of metadata from this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -parameters

### -param item [in]

Type: <b><a href="/previous-versions/ms534468(v=vs.85)">ImageItemData</a>*</b>

Pointer to an <a href="/previous-versions/ms534468(v=vs.85)">ImageItemData</a> object that specifies the item to be retrieved. The Data member of the <b>ImageItemData</b> object points to a buffer that receives the custom metadata. If the Data member is set to <b>NULL</b>, this method returns the size of the required buffer in the DataSize member of the ImageItemData object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>