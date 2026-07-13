---
UID: NF:icm.CMTranslateRGB
title: CMTranslateRGB
description: Translates an application-supplied RGBQuad into the device [color space](https://msdn.microsoft.com/en-us/library/dd371818\(v=vs.85\)).
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - icm32.dll
api_name:
 - CMTranslateRGB
f1_keywords:
 - CMTranslateRGB
 - icm/CMTranslateRGB
dev_langs:
 - c++
---

## -description

Translates an application-supplied RGBQuad into the device [color space](/windows/win32/wcs/c#color-space).

## -parameters

### -param hcmTransform

Specifies the transform to be used.

### -param ColorRef

The RGBQuad to translate.

### -param lpColorRef

Points to a buffer in which to place the translation.

### -param dwFlags

Specifies how the transform should be used to make the translation. This parameter can take one of the following meanings.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="CMS_FORWARD"></span><span id="cms_forward"></span>
<strong>CMS_FORWARD</strong></td>
<td><p>Use forward transform</p></td>
</tr>
<tr class="even">
<td><span id="CMS_BACKWARD"></span><span id="cms_backward"></span>
<strong>CMS_BACKWARD</strong></td>
<td><p>Use reverse transform</p></td>
</tr>
</tbody>
</table>

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. The CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

Every CMM is required to export this function.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
