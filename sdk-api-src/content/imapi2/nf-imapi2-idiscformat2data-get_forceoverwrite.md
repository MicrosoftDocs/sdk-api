---
UID: NF:imapi2.IDiscFormat2Data.get_ForceOverwrite
title: IDiscFormat2Data::get_ForceOverwrite (imapi2.h)
description: Determines if the data writer must overwrite the disc on overwritable media types. (Get)
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","get_ForceOverwrite method","IDiscFormat2Data.get_ForceOverwrite","IDiscFormat2Data::get_ForceOverwrite","get_ForceOverwrite","get_ForceOverwrite method [IMAPI]","get_ForceOverwrite method [IMAPI]","IDiscFormat2Data interface","imapi.idiscformat2data_get_forceoverwrite","imapi2/IDiscFormat2Data::get_ForceOverwrite"]
old-location: imapi\idiscformat2data_get_forceoverwrite.htm
tech.root: imapi
ms.assetid: ac1bfca7-e681-4e88-85d6-c77ffcbe7872
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_ForceOverwrite method, IDiscFormat2Data.get_ForceOverwrite, IDiscFormat2Data::get_ForceOverwrite, get_ForceOverwrite, get_ForceOverwrite method [IMAPI], get_ForceOverwrite method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_forceoverwrite, imapi2/IDiscFormat2Data::get_ForceOverwrite
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDiscFormat2Data::get_ForceOverwrite
 - imapi2/IDiscFormat2Data::get_ForceOverwrite
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
 - IDiscFormat2Data.get_ForceOverwrite
---

# IDiscFormat2Data::get_ForceOverwrite


## -description

Determines if the data writer must overwrite the disc on overwritable media types.

## -parameters

### -param value [out]

Is VARIANT_TRUE if the data writer must overwrite the disc on overwritable media types; otherwise, VARIANT_FALSE.

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

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>
