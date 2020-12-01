---
UID: NF:fci.FNFCIGETNEXTCABINET
title: FNFCIGETNEXTCABINET macro (fci.h)
description: The FNFCIGETNEXTCABINET macro provides the declaration for the application-defined callback function to request information for the next cabinet.
helpviewer_keywords: ["FNFCIGETNEXTCABINET","FNFCIGETNEXTCABINET macro [Windows API]","fci/FNFCIGETNEXTCABINET","winprog.fnfcigetnextcabinet"]
old-location: winprog\fnfcigetnextcabinet.htm
tech.root: winprog
ms.assetid: d56fb63e-91bf-4991-a954-176211697a2e
ms.date: 12/05/2018
ms.keywords: FNFCIGETNEXTCABINET, FNFCIGETNEXTCABINET macro [Windows API], fci/FNFCIGETNEXTCABINET, winprog.fnfcigetnextcabinet
req.header: fci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FNFCIGETNEXTCABINET
 - fci/FNFCIGETNEXTCABINET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCIGETNEXTCABINET
---

## -description

The <b>FNFCIGETNEXTCABINET</b> macro provides the declaration for the application-defined callback function to request information for the next cabinet.

## -parameters

### -param fn

Pointer to a <a href="/windows/desktop/api/fci/ns-fci-ccab">CCAB</a> structure to provide the parameters for the creation of a new cabinet.

## -remarks

The <a href="/windows/desktop/api/fci/ns-fci-ccab">CCAB</a> structure referenced by this function is relevant to the most recently completed cabinet. However, with each successful operation the  <i>iCab</i> field contained within this structure will have incremented by 1. Additionally, the next cabinet will be created using the fields in this structure.  The szCab, in particular, should be modified as necessary. In particular, the <i>szCab</i> field, which specifies the cabinet name, should be changed for each cabinet.

When creating multiple cabinets, typically the <i>iCab</i> field is used to create the name.


#### Examples


```cpp
FNFCIGETNEXTCABINET(fnGetNextCabinet)
{
    HRESULT hr;

    UNREFERENCED_PARAMETER(pv);
    UNREFERENCED_PARAMETER(cbPrevCab);
    
    hr = StringCchPrintfA(pccab->szCab,
                          ARRAYSIZE(pccab->szCab),
                          "FCISample%02d.cab",
                          pccab->iCab);
        
    return ( SUCCEEDED(hr) );
}

```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>