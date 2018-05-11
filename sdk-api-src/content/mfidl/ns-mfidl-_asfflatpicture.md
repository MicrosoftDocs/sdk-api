---
UID: NS:mfidl._ASFFlatPicture
title: "_ASFFlatPicture"
author: windows-driver-content
description: Contains an image that is stored as metadata for a media source. This structure is used as the data item for the WM/Picture metadata attribute.
old-location: mf\asf_flat_picture.htm
old-project: medfound
ms.assetid: 2aa190bd-3431-4f37-bf2b-0801047793b3
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 2aa190bd-3431-4f37-bf2b-0801047793b3, ASF_FLAT_PICTURE, ASF_FLAT_PICTURE structure [Media Foundation], _ASFFlatPicture, mf.asf_flat_picture, mfidl/ASF_FLAT_PICTURE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfidl.h
req.include-header: 
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
req.typenames: ASF_FLAT_PICTURE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfidl.h
api_name:
-	ASF_FLAT_PICTURE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ASFFlatPicture structure


## -description



Contains an image that is stored as metadata for a media source. This structure is used as the data item for the <a href="wmformat.wm_picture_attribute">WM/Picture</a> metadata attribute.




## -struct-fields




### -field bPictureType


            Specifies the type of image. This member is equivalent to the <b>bPictureType</b> member in the <a href="https://msdn.microsoft.com/d3670cce-5b57-4624-b10d-2e4d9e9e263c">WM_PICTURE</a> structure. 
          


### -field dwDataLen


            Size, in bytes, of the image data.
          


## -remarks



The <a href="wmformat.wm_picture_attribute">WM/Picture</a> attribute is defined in the Windows Media Format SDK. The attribute contains a picture related to the content, such as album art.

To get this attribute from a media source, call <a href="https://msdn.microsoft.com/177c8612-5c9f-4a71-9ee1-a4c67737af2d">IMFMetadata::GetProperty</a>, passing in the constant g_wszWMPicture for the <i>pwszName</i> parameter. The method retrieves a <b>PROPVARIANT</b> that contains a binary array (VT_BLOB). The layout of the array is as follows:

<ul>
<li><b>ASF_FLAT_PICTURE</b> structure.
          </li>
<li>
            Null-terminated wide-character string that contains the MIME type.
          </li>
<li>
            Null-terminated wide-character string that contains a description.
          </li>
<li>
Image data.

</li>
</ul>
This format differs from the <a href="https://msdn.microsoft.com/d3670cce-5b57-4624-b10d-2e4d9e9e263c">WM_PICTURE</a> structure used in the Windows Media Format SDK. The <b>WM_PICTURE</b> structure contains internal pointers to two strings and the image data. If the structure is copied, these pointers become invalid. The <b>ASF_FLAT_PICTURE</b> structure does not contain internal pointers, so it is safe to copy the structure.




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

