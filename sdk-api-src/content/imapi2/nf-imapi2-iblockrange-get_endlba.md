---
UID: NF:imapi2.IBlockRange.get_EndLba
title: IBlockRange::get_EndLba (imapi2.h)
description: Retrieves the end sector of the range specified by the IBlockRange interface.
helpviewer_keywords: ["IBlockRange interface [IMAPI]","get_EndLba method","IBlockRange.get_EndLba","IBlockRange::get_EndLba","get_EndLba","get_EndLba method [IMAPI]","get_EndLba method [IMAPI]","IBlockRange interface","imapi.iblockrange_get_endlba","imapi2/IBlockRange::get_EndLba"]
old-location: imapi\iblockrange_get_endlba.htm
tech.root: imapi
ms.assetid: e2260241-5922-4cf5-8aff-1dd7431a44c2
ms.date: 12/05/2018
ms.keywords: IBlockRange interface [IMAPI],get_EndLba method, IBlockRange.get_EndLba, IBlockRange::get_EndLba, get_EndLba, get_EndLba method [IMAPI], get_EndLba method [IMAPI],IBlockRange interface, imapi.iblockrange_get_endlba, imapi2/IBlockRange::get_EndLba
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IBlockRange::get_EndLba
 - imapi2/IBlockRange::get_EndLba
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IBlockRange.get_EndLba
---

# IBlockRange::get_EndLba


## -description

Retrieves the end sector of the range specified by the <a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange">IBlockRange</a> interface.

## -parameters

### -param value [out]

The end sector of the range.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt>Value: 0x80004003</dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -remarks

The sector number returned by this method is included in the range.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange">IBlockRange</a>