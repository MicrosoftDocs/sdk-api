---
UID: NF:ocidl.IFont.put_Weight
title: IFont::put_Weight (ocidl.h)
description: Sets the font's Weight property.
helpviewer_keywords: ["IFont interface [COM]","put_Weight method","IFont.put_Weight","IFont::put_Weight","_ctrl_ifont_put_weight","com.ifont_put_weight","ocidl/IFont::put_Weight","put_Weight","put_Weight method [COM]","put_Weight method [COM]","IFont interface"]
old-location: com\ifont_put_weight.htm
tech.root: com
ms.assetid: 716c77f3-6224-40d7-abea-46ed5eedb08a
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],put_Weight method, IFont.put_Weight, IFont::put_Weight, _ctrl_ifont_put_weight, com.ifont_put_weight, ocidl/IFont::put_Weight, put_Weight, put_Weight method [COM], put_Weight method [COM],IFont interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFont::put_Weight
 - ocidl/IFont::put_Weight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.put_Weight
---

# IFont::put_Weight


## -description

Sets the font's Weight property.

## -parameters

### -param weight [in]

The new Weight for the font. For a list of available font weights, see the description of the <b>lfWeight</b> member of 
    the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The Weight property was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This font does not support different weights. This value is not an error condition.

</td>
</tr>
</table>

## -remarks

This property may 
   affect the Bold property as well. The Bold 
   property is set to <b>TRUE</b> if the Weight property is 
   greater than the average of <b>FW_NORMAL</b> (400) and <b>FW_BOLD</b> (700), 
   that is 550.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_weight">IFont::get_Weight</a>