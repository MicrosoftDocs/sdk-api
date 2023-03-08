---
UID: NN:imapi2.IBurnVerification
title: IBurnVerification (imapi2.h)
description: Use this interface with IDiscFormat2Data or IDiscFormat2TrackAtOnce to get or set the Burn Verification Level property which dictates how burned media is verified for integrity after the write operation.
helpviewer_keywords: ["IBurnVerification","IBurnVerification interface [IMAPI]","IBurnVerification interface [IMAPI]","described","imapi.iburnverification","imapi2/IBurnVerification"]
old-location: imapi\iburnverification.htm
tech.root: imapi
ms.assetid: 3a410ab8-dfc3-4c30-a198-3888ed750a6d
ms.date: 12/05/2018
ms.keywords: IBurnVerification, IBurnVerification interface [IMAPI], IBurnVerification interface [IMAPI],described, imapi.iburnverification, imapi2/IBurnVerification
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
 - IBurnVerification
 - imapi2/IBurnVerification
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
 - IBurnVerification
---

# IBurnVerification interface


## -description

Use  this interface with  <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a> or <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a> to get or set the Burn Verification Level property which dictates how burned media is verified for integrity after the write operation.

## -inheritance

The <b>IBurnVerification</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBurnVerification</b> also has these types of members:

## -remarks

The following example function demonstrates how the burn verification level defined by <a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_burn_verification_level">IMAPI_BURN_VERIFICATION_LEVEL</a>, can be implemented. Burn verification level should be set prior to a burn operation.


```cpp
#include <imapi2.h>

HRESULT setBurnVerification(
    IDiscFormat2Data                *DataWriter,
    IMAPI_BURN_VERIFICATION_LEVEL   VerificationLevel
    )

{
    HRESULT hr = S_OK;
    IBurnVerification *burnVerifier = NULL;
 
    hr = DataWriter->QueryInterface(IID_PPV_ARGS(&burnVerifier));
 
    if (SUCCEEDED(hr))
    {
        hr = burnVerifier->put_BurnVerificationLevel(VerificationLevel);
    }
 
    if (burnVerifier != NULL)
    {
        burnVerifier->Release();
        burnVerifier = NULL;
    }
 
    return hr;
}

```


This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_burn_verification_level">IMAPI_BURN_VERIFICATION_LEVEL</a>
