---
UID: NS:richedit.tagRICHEDIT_IMAGE_PARAMETERS
title: RICHEDIT_IMAGE_PARAMETERS (richedit.h)
description: Defines the attributes of an image to be inserted by the EM_INSERTIMAGE message.
helpviewer_keywords: ["RICHEDIT_IMAGE_PARAMETERS","RICHEDIT_IMAGE_PARAMETERS structure [Windows Controls]","TA_BASELINE","TA_BOTTOM","TA_TOP","controls.richedit_image_parameters","richedit/RICHEDIT_IMAGE_PARAMETERS"]
old-location: controls\richedit_image_parameters.htm
tech.root: Controls
ms.assetid: 9FBEB9BE-B27E-4AC6-AB39-1DBCF74AED8B
ms.date: 12/05/2018
ms.keywords: RICHEDIT_IMAGE_PARAMETERS, RICHEDIT_IMAGE_PARAMETERS structure [Windows Controls], TA_BASELINE, TA_BOTTOM, TA_TOP, controls.richedit_image_parameters, richedit/RICHEDIT_IMAGE_PARAMETERS
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: RICHEDIT_IMAGE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRICHEDIT_IMAGE_PARAMETERS
 - richedit/tagRICHEDIT_IMAGE_PARAMETERS
 - RICHEDIT_IMAGE_PARAMETERS
 - richedit/RICHEDIT_IMAGE_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - RICHEDIT_IMAGE_PARAMETERS
---

# RICHEDIT_IMAGE_PARAMETERS structure


## -description

Defines the attributes of an image to be inserted by the <a href="/windows/desktop/Controls/em-insertimage">EM_INSERTIMAGE</a> message.

## -struct-fields

### -field xWidth

The width, in HIMETRIC units (0.01 mm), of the image.

### -field yHeight

### -field Ascent

If <i>Type</i> is TA_BASELINE, this parameter is the distance, in HIMETRIC units, that the top of the image extends above the text baseline. If <i>Type</i> is TA_BASELINE and ascent is zero, the bottom of the image is placed at the text baseline.

### -field Type

The vertical alignment of the image. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TA_BASELINE"></a><a id="ta_baseline"></a><dl>
<dt><b>TA_BASELINE</b></dt>
</dl>
</td>
<td width="60%">
Align the image relative to the text baseline. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_BOTTOM"></a><a id="ta_bottom"></a><dl>
<dt><b>TA_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Align the bottom of the image at the bottom of the text line. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_TOP"></a><a id="ta_top"></a><dl>
<dt><b>TA_TOP</b></dt>
</dl>
</td>
<td width="60%">
Align the top of the image at the top of the text line

</td>
</tr>
</table>

### -field pwszAlternateText

The alternate text for the image.

### -field pIStream

The stream that contains the image data.


#### - xHeight

The height, in HIMETRIC units, of the image.

## -see-also

<a href="/windows/desktop/Controls/em-insertimage">EM_INSERTIMAGE</a>