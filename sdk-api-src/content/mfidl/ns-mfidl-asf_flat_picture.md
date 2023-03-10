---
UID: NS:mfidl._ASFFlatPicture
title: ASF_FLAT_PICTURE (mfidl.h)
description: Contains an image that is stored as metadata for a media source. This structure is used as the data item for the WM/Picture metadata attribute.
helpviewer_keywords: ["2aa190bd-3431-4f37-bf2b-0801047793b3","ASF_FLAT_PICTURE","ASF_FLAT_PICTURE structure [Media Foundation]","mf.asf_flat_picture","mfidl/ASF_FLAT_PICTURE"]
old-location: mf\asf_flat_picture.htm
tech.root: mf
ms.assetid: 2aa190bd-3431-4f37-bf2b-0801047793b3
ms.date: 12/05/2018
ms.keywords: 2aa190bd-3431-4f37-bf2b-0801047793b3, ASF_FLAT_PICTURE, ASF_FLAT_PICTURE structure [Media Foundation], mf.asf_flat_picture, mfidl/ASF_FLAT_PICTURE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ASF_FLAT_PICTURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ASFFlatPicture
 - mfidl/_ASFFlatPicture
 - ASF_FLAT_PICTURE
 - mfidl/ASF_FLAT_PICTURE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - ASF_FLAT_PICTURE
---

# ASF_FLAT_PICTURE structure


## -description

Contains an image that is stored as metadata for a media source. This structure is used as the data item for the <a href="/windows/desktop/wmformat/wmpicture">WM/Picture</a> metadata attribute.

## -struct-fields

### -field bPictureType

Specifies the type of image. This member is equivalent to the <b>bPictureType</b> member in the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture">WM_PICTURE</a> structure.

### -field dwDataLen

Size, in bytes, of the image data.

## -remarks

The <a href="/windows/desktop/wmformat/wmpicture">WM/Picture</a> attribute is defined in the Windows Media Format SDK. The attribute contains a picture related to the content, such as album art.

To get this attribute from a media source, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty">IMFMetadata::GetProperty</a>, passing in the constant g_wszWMPicture for the <i>pwszName</i> parameter. The method retrieves a <b>PROPVARIANT</b> that contains a binary array (VT_BLOB). The layout of the array is as follows:

<ul>
<li><b>ASF_FLAT_PICTURE</b> structure.
          </li>
<li>Null-terminated wide-character string that contains the MIME type.
          </li>
<li>Null-terminated wide-character string that contains a description.
          </li>
<li>
Image data.

</li>
</ul>
This format differs from the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture">WM_PICTURE</a> structure used in the Windows Media Format SDK. The <b>WM_PICTURE</b> structure contains internal pointers to two strings and the image data. If the structure is copied, these pointers become invalid. The <b>ASF_FLAT_PICTURE</b> structure does not contain internal pointers, so it is safe to copy the structure.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>