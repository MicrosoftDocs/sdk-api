---
UID: NS:wincrypt._CERT_LOGOTYPE_IMAGE_INFO
title: CERT_LOGOTYPE_IMAGE_INFO (wincrypt.h)
description: Contains more detailed information about an image logotype.
helpviewer_keywords: ["*PCERT_LOGOTYPE_IMAGE_INFO","CERT_LOGOTYPE_BITS_IMAGE_RESOLUTION_CHOICE","CERT_LOGOTYPE_COLOR_IMAGE_INFO_CHOICE","CERT_LOGOTYPE_GRAY_SCALE_IMAGE_INFO_CHOICE","CERT_LOGOTYPE_IMAGE_INFO","CERT_LOGOTYPE_IMAGE_INFO structure [Security]","CERT_LOGOTYPE_NO_IMAGE_RESOLUTION_CHOICE","CERT_LOGOTYPE_TABLE_SIZE_IMAGE_RESOLUTION_CHOICE","PCERT_LOGOTYPE_IMAGE_INFO","PCERT_LOGOTYPE_IMAGE_INFO structure pointer [Security]","security.cert_logotype_image_info","wincrypt/CERT_LOGOTYPE_IMAGE_INFO","wincrypt/PCERT_LOGOTYPE_IMAGE_INFO"]
old-location: security\cert_logotype_image_info.htm
tech.root: security
ms.assetid: d7116e54-dbf2-457e-8d33-1c0fd5641fe7
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_IMAGE_INFO, CERT_LOGOTYPE_BITS_IMAGE_RESOLUTION_CHOICE, CERT_LOGOTYPE_COLOR_IMAGE_INFO_CHOICE, CERT_LOGOTYPE_GRAY_SCALE_IMAGE_INFO_CHOICE, CERT_LOGOTYPE_IMAGE_INFO, CERT_LOGOTYPE_IMAGE_INFO structure [Security], CERT_LOGOTYPE_NO_IMAGE_RESOLUTION_CHOICE, CERT_LOGOTYPE_TABLE_SIZE_IMAGE_RESOLUTION_CHOICE, PCERT_LOGOTYPE_IMAGE_INFO, PCERT_LOGOTYPE_IMAGE_INFO structure pointer [Security], security.cert_logotype_image_info, wincrypt/CERT_LOGOTYPE_IMAGE_INFO, wincrypt/PCERT_LOGOTYPE_IMAGE_INFO'
req.header: wincrypt.h
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
req.typenames: CERT_LOGOTYPE_IMAGE_INFO, *PCERT_LOGOTYPE_IMAGE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_IMAGE_INFO
 - wincrypt/_CERT_LOGOTYPE_IMAGE_INFO
 - PCERT_LOGOTYPE_IMAGE_INFO
 - wincrypt/PCERT_LOGOTYPE_IMAGE_INFO
 - CERT_LOGOTYPE_IMAGE_INFO
 - wincrypt/CERT_LOGOTYPE_IMAGE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_LOGOTYPE_IMAGE_INFO
---

# CERT_LOGOTYPE_IMAGE_INFO structure


## -description

The <b>CERT_LOGOTYPE_IMAGE_INFO</b> structure contains more detailed information about an image logotype.

## -struct-fields

### -field dwLogotypeImageInfoChoice

Specifies the type of image. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_GRAY_SCALE_IMAGE_INFO_CHOICE"></a><a id="cert_logotype_gray_scale_image_info_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_GRAY_SCALE_IMAGE_INFO_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The image is a grayscale image.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_COLOR_IMAGE_INFO_CHOICE"></a><a id="cert_logotype_color_image_info_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_COLOR_IMAGE_INFO_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The image is a color image.

</td>
</tr>
</table>

### -field dwFileSize

The size, in octets, of the image.

### -field dwXSize

The horizontal size, in pixels, of the image.

### -field dwYSize

The vertical size, in pixels, of the image.

### -field dwLogotypeImageResolutionChoice

Specifies the format of the image resolution. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_NO_IMAGE_RESOLUTION_CHOICE"></a><a id="cert_logotype_no_image_resolution_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_NO_IMAGE_RESOLUTION_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
No image resolution information is provided.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_BITS_IMAGE_RESOLUTION_CHOICE"></a><a id="cert_logotype_bits_image_resolution_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_BITS_IMAGE_RESOLUTION_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The image resolution is provided in bits per pixel. The <b>dwNumBits</b> member contains the image resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_TABLE_SIZE_IMAGE_RESOLUTION_CHOICE"></a><a id="cert_logotype_table_size_image_resolution_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_TABLE_SIZE_IMAGE_RESOLUTION_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The image resolution is provided in number of gray tones. The <b>dwTableSize</b> member contains the image resolution.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.dwNumBits

The resolution of the image, in bits per pixel. The member is only used if the <b>dwLogotypeImageResolutionChoice</b> contains <b>CERT_LOGOTYPE_NO_IMAGE_RESOLUTION_CHOICE</b>.

### -field DUMMYUNIONNAME.dwTableSize

The resolution of the image, in number of gray tones. The member is only used if the <b>dwLogotypeImageResolutionChoice</b> contains <b>CERT_LOGOTYPE_TABLE_SIZE_IMAGE_RESOLUTION_CHOICE</b>.

### -field pwszLanguage

The address of a null-terminated IA5 string that contains the RFC 3066 language identifier that specifies the language of the image. This member is optional and may be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_image">CERT_LOGOTYPE_IMAGE</a>