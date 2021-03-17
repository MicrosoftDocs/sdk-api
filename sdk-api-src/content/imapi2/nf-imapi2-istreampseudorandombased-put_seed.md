---
UID: NF:imapi2.IStreamPseudoRandomBased.put_Seed
title: IStreamPseudoRandomBased::put_Seed (imapi2.h)
description: Sets the seed value used by the random number generator and seeks to the start of stream.
helpviewer_keywords: ["IStreamPseudoRandomBased interface [IMAPI]","put_Seed method","IStreamPseudoRandomBased.put_Seed","IStreamPseudoRandomBased::put_Seed","imapi.istreampseudorandombased_put_seed","imapi2/IStreamPseudoRandomBased::put_Seed","put_Seed","put_Seed method [IMAPI]","put_Seed method [IMAPI]","IStreamPseudoRandomBased interface"]
old-location: imapi\istreampseudorandombased_put_seed.htm
tech.root: imapi
ms.assetid: 455d087d-a6f5-45ab-9c0d-c46e721cba6e
ms.date: 12/05/2018
ms.keywords: IStreamPseudoRandomBased interface [IMAPI],put_Seed method, IStreamPseudoRandomBased.put_Seed, IStreamPseudoRandomBased::put_Seed, imapi.istreampseudorandombased_put_seed, imapi2/IStreamPseudoRandomBased::put_Seed, put_Seed, put_Seed method [IMAPI], put_Seed method [IMAPI],IStreamPseudoRandomBased interface
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
 - IStreamPseudoRandomBased::put_Seed
 - imapi2/IStreamPseudoRandomBased::put_Seed
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
 - IStreamPseudoRandomBased.put_Seed
---

# IStreamPseudoRandomBased::put_Seed


## -description

Sets the seed value used by the random number generator and seeks to the start of stream.

## -parameters

### -param value [in]

Seed value for the random number generator.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased">IStreamPseudoRandomBased</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-get_seed">IStreamPseudoRandomBased::get_Seed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreampseudorandombased-put_extendedseed">IStreamPseudoRandomBased::put_ExtendedSeed</a>