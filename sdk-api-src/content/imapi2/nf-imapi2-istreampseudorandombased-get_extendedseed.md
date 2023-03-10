---
UID: NF:imapi2.IStreamPseudoRandomBased.get_ExtendedSeed
title: IStreamPseudoRandomBased::get_ExtendedSeed (imapi2.h)
description: Retrieves an array of seed values used by the random number generator.
helpviewer_keywords: ["IStreamPseudoRandomBased interface [IMAPI]","get_ExtendedSeed method","IStreamPseudoRandomBased.get_ExtendedSeed","IStreamPseudoRandomBased::get_ExtendedSeed","get_ExtendedSeed","get_ExtendedSeed method [IMAPI]","get_ExtendedSeed method [IMAPI]","IStreamPseudoRandomBased interface","imapi.istreampseudorandombased_get_extendedseed","imapi2/IStreamPseudoRandomBased::get_ExtendedSeed"]
old-location: imapi\istreampseudorandombased_get_extendedseed.htm
tech.root: imapi
ms.assetid: e15e47aa-e5c4-4944-a3c4-14e459a31bb5
ms.date: 12/05/2018
ms.keywords: IStreamPseudoRandomBased interface [IMAPI],get_ExtendedSeed method, IStreamPseudoRandomBased.get_ExtendedSeed, IStreamPseudoRandomBased::get_ExtendedSeed, get_ExtendedSeed, get_ExtendedSeed method [IMAPI], get_ExtendedSeed method [IMAPI],IStreamPseudoRandomBased interface, imapi.istreampseudorandombased_get_extendedseed, imapi2/IStreamPseudoRandomBased::get_ExtendedSeed
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
 - IStreamPseudoRandomBased::get_ExtendedSeed
 - imapi2/IStreamPseudoRandomBased::get_ExtendedSeed
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
 - IStreamPseudoRandomBased.get_ExtendedSeed
---

# IStreamPseudoRandomBased::get_ExtendedSeed


## -description

Retrieves an array of seed values used by the random number generator.

## -parameters

### -param values [out]

Array of seed values used by the random number generator.

### -param eCount [out]

Number of seed values in the <i>values</i> array.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased">IStreamPseudoRandomBased</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-get_seed">IStreamPseudoRandomBased::get_Seed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-put_extendedseed">IStreamPseudoRandomBased::put_ExtendedSeed</a>