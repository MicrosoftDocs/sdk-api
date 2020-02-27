---
UID: NF:mfapi.MFSetAttributeRatio
title: MFSetAttributeRatio function (mfapi.h)
description: Sets a ratio as a 64-bit attribute value.
old-location: mf\mfsetattributeratio.htm
tech.root: medfound
ms.assetid: 04e8c89e-115e-41d4-b8cb-953f68ddd14e
ms.date: 12/05/2018
ms.keywords: 04e8c89e-115e-41d4-b8cb-953f68ddd14e, MFSetAttributeRatio, MFSetAttributeRatio function [Media Foundation], mf.mfsetattributeratio, mfapi/MFSetAttributeRatio
f1_keywords:
- mfapi/MFSetAttributeRatio
dev_langs:
- c++
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mfapi.h
api_name:
- MFSetAttributeRatio
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFSetAttributeRatio function


## -description


Sets a ratio as a 64-bit attribute value.
        


## -parameters




### -param pAttributes [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.
          


### -param guidKey [in]

A 
            
              <b>GUID</b> that identifies the value to set. If this key already exists, the function overwrites the old value.
          


### -param unNumerator [in]

The numerator of the ratio.
          


### -param unDenominator [in]

The denominator of the ratio.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Some attributes specify a ratio as a packed <b>UINT64</b> value. This function packs the numerator and denominator into a single <b>UINT64</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio">MFGetAttributeRatio</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

