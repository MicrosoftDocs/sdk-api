---
UID: NF:imapi2.IStreamPseudoRandomBased.get_Seed
title: IStreamPseudoRandomBased::get_Seed (imapi2.h)
description: Retrieves the seed value used by the random number generator.
helpviewer_keywords: ["IStreamPseudoRandomBased interface [IMAPI]","get_Seed method","IStreamPseudoRandomBased.get_Seed","IStreamPseudoRandomBased::get_Seed","get_Seed","get_Seed method [IMAPI]","get_Seed method [IMAPI]","IStreamPseudoRandomBased interface","imapi.istreampseudorandombased_get_seed","imapi2/IStreamPseudoRandomBased::get_Seed"]
old-location: imapi\istreampseudorandombased_get_seed.htm
tech.root: imapi
ms.assetid: c5362760-84c6-4e93-b3cd-2ce568b13102
ms.date: 12/05/2018
ms.keywords: IStreamPseudoRandomBased interface [IMAPI],get_Seed method, IStreamPseudoRandomBased.get_Seed, IStreamPseudoRandomBased::get_Seed, get_Seed, get_Seed method [IMAPI], get_Seed method [IMAPI],IStreamPseudoRandomBased interface, imapi.istreampseudorandombased_get_seed, imapi2/IStreamPseudoRandomBased::get_Seed
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
 - IStreamPseudoRandomBased::get_Seed
 - imapi2/IStreamPseudoRandomBased::get_Seed
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
 - IStreamPseudoRandomBased.get_Seed
---

# IStreamPseudoRandomBased::get_Seed


## -description

Retrieves the seed value used by the random number generator.

## -parameters

### -param value [out]

Seed value for the random number generator.

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

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased">IStreamPseudoRandomBased</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-get_extendedseed">IStreamPseudoRandomBased::get_ExtendedSeed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-put_seed">IStreamPseudoRandomBased::put_Seed</a>