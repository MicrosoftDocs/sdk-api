---
UID: NF:imapi2.IStreamPseudoRandomBased.put_ExtendedSeed
title: IStreamPseudoRandomBased::put_ExtendedSeed (imapi2.h)
description: Sets a list of seed values for the random number generator and seeks to the start of stream.
helpviewer_keywords: ["IStreamPseudoRandomBased interface [IMAPI]","put_ExtendedSeed method","IStreamPseudoRandomBased.put_ExtendedSeed","IStreamPseudoRandomBased::put_ExtendedSeed","imapi.istreampseudorandombased_put_extendedseed","imapi2/IStreamPseudoRandomBased::put_ExtendedSeed","put_ExtendedSeed","put_ExtendedSeed method [IMAPI]","put_ExtendedSeed method [IMAPI]","IStreamPseudoRandomBased interface"]
old-location: imapi\istreampseudorandombased_put_extendedseed.htm
tech.root: imapi
ms.assetid: a6edf21f-b89a-4780-8065-4d09758fe701
ms.date: 12/05/2018
ms.keywords: IStreamPseudoRandomBased interface [IMAPI],put_ExtendedSeed method, IStreamPseudoRandomBased.put_ExtendedSeed, IStreamPseudoRandomBased::put_ExtendedSeed, imapi.istreampseudorandombased_put_extendedseed, imapi2/IStreamPseudoRandomBased::put_ExtendedSeed, put_ExtendedSeed, put_ExtendedSeed method [IMAPI], put_ExtendedSeed method [IMAPI],IStreamPseudoRandomBased interface
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
 - IStreamPseudoRandomBased::put_ExtendedSeed
 - imapi2/IStreamPseudoRandomBased::put_ExtendedSeed
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
 - IStreamPseudoRandomBased.put_ExtendedSeed
---

# IStreamPseudoRandomBased::put_ExtendedSeed


## -description

Sets a list of seed values for the random number generator and seeks to the start of stream.<div class="alert"><b>Note</b>  This interface is currently not implemented.</div>
<div> </div>

## -parameters

### -param values [in]

Array of seed values used by the random number generator.

### -param eCount [in]

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

## -remarks

Use this method to provide a seed value greater than 32 bits.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased">IStreamPseudoRandomBased</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-get_extendedseed">IStreamPseudoRandomBased::get_ExtendedSeed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-put_seed">IStreamPseudoRandomBased::put_Seed</a>