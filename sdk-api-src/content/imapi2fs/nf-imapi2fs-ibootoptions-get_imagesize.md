---
UID: NF:imapi2fs.IBootOptions.get_ImageSize
title: IBootOptions::get_ImageSize (imapi2fs.h)
description: Retrieves the size of the boot image.
helpviewer_keywords: ["IBootOptions interface [IMAPI]","get_ImageSize method","IBootOptions.get_ImageSize","IBootOptions::get_ImageSize","get_ImageSize","get_ImageSize method [IMAPI]","get_ImageSize method [IMAPI]","IBootOptions interface","imapi.ibootoptions_get_imagesize","imapi2fs/IBootOptions::get_ImageSize"]
old-location: imapi\ibootoptions_get_imagesize.htm
tech.root: imapi
ms.assetid: 2e3fd791-5a38-4082-9553-29eae92dfd5e
ms.date: 12/05/2018
ms.keywords: IBootOptions interface [IMAPI],get_ImageSize method, IBootOptions.get_ImageSize, IBootOptions::get_ImageSize, get_ImageSize, get_ImageSize method [IMAPI], get_ImageSize method [IMAPI],IBootOptions interface, imapi.ibootoptions_get_imagesize, imapi2fs/IBootOptions::get_ImageSize
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IBootOptions::get_ImageSize
 - imapi2fs/IBootOptions::get_ImageSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IBootOptions.get_ImageSize
---

# IBootOptions::get_ImageSize


## -description

Retrieves the size of the boot image.

## -parameters

### -param pVal [out]

Size, in bytes, of the boot image.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a>