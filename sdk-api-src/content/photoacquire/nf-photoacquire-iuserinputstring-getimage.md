---
UID: NF:photoacquire.IUserInputString.GetImage
title: IUserInputString::GetImage (photoacquire.h)
description: The GetImage method retrieves the default image used to initialize an edit control.
helpviewer_keywords: ["GetImage","GetImage method [Picture Acquisition]","GetImage method [Picture Acquisition]","IUserInputString interface","IUserInputString interface [Picture Acquisition]","GetImage method","IUserInputString.GetImage","IUserInputString::GetImage","IUserInputStringGetImage","photoacquire/IUserInputString::GetImage","picacq.iuserinputstring_getimage"]
old-location: picacq\iuserinputstring_getimage.htm
tech.root: picacq
ms.assetid: a626c53d-b9dd-483b-924d-6f5d2d1c2663
ms.date: 12/05/2018
ms.keywords: GetImage, GetImage method [Picture Acquisition], GetImage method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetImage method, IUserInputString.GetImage, IUserInputString::GetImage, IUserInputStringGetImage, photoacquire/IUserInputString::GetImage, picacq.iuserinputstring_getimage
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserInputString::GetImage
 - photoacquire/IUserInputString::GetImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IUserInputString.GetImage
---

# IUserInputString::GetImage


## -description

The <code>GetImage</code> method retrieves the default image used to initialize an edit control.

## -parameters

### -param nSize [in]

Integer containing the size of the image.

### -param phBitmap [out]

Pointer to the handle that specifies the image bitmap.

### -param phIcon [out]

Pointer to the handle that specifies the image icon.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed where a non-<b>NULL</b> pointer is expected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString Interface</a>