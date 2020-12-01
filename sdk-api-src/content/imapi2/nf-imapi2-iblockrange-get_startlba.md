---
UID: NF:imapi2.IBlockRange.get_StartLba
title: IBlockRange::get_StartLba (imapi2.h)
description: Retrieves the start sector of the range described by IBlockRange.
helpviewer_keywords: ["IBlockRange interface [IMAPI]","get_StartLba method","IBlockRange.get_StartLba","IBlockRange::get_StartLba","get_StartLba","get_StartLba method [IMAPI]","get_StartLba method [IMAPI]","IBlockRange interface","imapi.iblockrange_get_startlba","imapi2/IBlockRange::get_StartLba"]
old-location: imapi\iblockrange_get_startlba.htm
tech.root: imapi
ms.assetid: 6891aebd-3795-4e1c-a065-1579a984de41
ms.date: 12/05/2018
ms.keywords: IBlockRange interface [IMAPI],get_StartLba method, IBlockRange.get_StartLba, IBlockRange::get_StartLba, get_StartLba, get_StartLba method [IMAPI], get_StartLba method [IMAPI],IBlockRange interface, imapi.iblockrange_get_startlba, imapi2/IBlockRange::get_StartLba
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
 - IBlockRange::get_StartLba
 - imapi2/IBlockRange::get_StartLba
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
 - IBlockRange.get_StartLba
---

# IBlockRange::get_StartLba


## -description

Retrieves the start sector of the range described by <a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange">IBlockRange</a>.

## -parameters

### -param value [out]

The start sector of the range.

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

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange">IBlockRange</a>