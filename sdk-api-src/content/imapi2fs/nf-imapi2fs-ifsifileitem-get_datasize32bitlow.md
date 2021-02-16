---
UID: NF:imapi2fs.IFsiFileItem.get_DataSize32BitLow
title: IFsiFileItem::get_DataSize32BitLow (imapi2fs.h)
description: Retrieves the least significant 32 bits of the IFsiFileItem::get_DataSize property.
helpviewer_keywords: ["IFsiFileItem interface [IMAPI]","get_DataSize32BitLow method","IFsiFileItem.get_DataSize32BitLow","IFsiFileItem::get_DataSize32BitLow","get_DataSize32BitLow","get_DataSize32BitLow method [IMAPI]","get_DataSize32BitLow method [IMAPI]","IFsiFileItem interface","imapi.ifsifileitem_get_datasize32bitlow","imapi2fs/IFsiFileItem::get_DataSize32BitLow"]
old-location: imapi\ifsifileitem_get_datasize32bitlow.htm
tech.root: imapi
ms.assetid: beeec2bc-5f0e-4a53-afed-50c0b6069f54
ms.date: 12/05/2018
ms.keywords: IFsiFileItem interface [IMAPI],get_DataSize32BitLow method, IFsiFileItem.get_DataSize32BitLow, IFsiFileItem::get_DataSize32BitLow, get_DataSize32BitLow, get_DataSize32BitLow method [IMAPI], get_DataSize32BitLow method [IMAPI],IFsiFileItem interface, imapi.ifsifileitem_get_datasize32bitlow, imapi2fs/IFsiFileItem::get_DataSize32BitLow
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
 - IFsiFileItem::get_DataSize32BitLow
 - imapi2fs/IFsiFileItem::get_DataSize32BitLow
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
 - IFsiFileItem.get_DataSize32BitLow
---

# IFsiFileItem::get_DataSize32BitLow


## -description

Retrieves the least significant 32 bits of the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_datasize">IFsiFileItem::get_DataSize</a> property.

## -parameters

### -param pVal [out]

Least significant 32 bits of the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_datasize">IFsiFileItem::get_DataSize</a> property.

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

## -remarks

This property and <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_datasize32bithigh">IFsiFileItem::get_DataSize32BitHigh</a> together  provide the size of the file as two 32-bit numbers for languages that do not support 64-bit values, such as VBScript and Visual Basic 6.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_datasize">IFsiFileItem::get_DataSize</a>