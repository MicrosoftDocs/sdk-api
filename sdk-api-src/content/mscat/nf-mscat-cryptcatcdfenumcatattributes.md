---
UID: NF:mscat.CryptCATCDFEnumCatAttributes
title: CryptCATCDFEnumCatAttributes function (mscat.h)
description: Enumerates catalog-level attributes within the CatalogHeader section of a catalog definition file (CDF).
helpviewer_keywords: ["CryptCATCDFEnumCatAttributes","CryptCATCDFEnumCatAttributes function [Security]","mscat/CryptCATCDFEnumCatAttributes","security.cryptcatcdfenumcatattributes"]
old-location: security\cryptcatcdfenumcatattributes.htm
tech.root: security
ms.assetid: 01889cb9-7bf4-4591-9bb2-b263c4effe0c
ms.date: 12/05/2018
ms.keywords: CryptCATCDFEnumCatAttributes, CryptCATCDFEnumCatAttributes function [Security], mscat/CryptCATCDFEnumCatAttributes, security.cryptcatcdfenumcatattributes
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATCDFEnumCatAttributes
 - mscat/CryptCATCDFEnumCatAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATCDFEnumCatAttributes
---

# CryptCATCDFEnumCatAttributes function


## -description

<p class="CCE_Message">[The  <b>CryptCATCDFEnumCatAttributes</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATCDFEnumCatAttributes</b> function enumerates catalog-level attributes within the <b>CatalogHeader</b> section of a catalog definition file (CDF). <b>CryptCATCDFEnumCatAttributes</b> is called by <a href="/windows/desktop/SecCrypto/makecat">MakeCat</a>.

## -parameters

### -param pCDF [in]

A pointer to a [CRYPTCATCDF](/windows/desktop/api/mscat/ns-mscat-cryptcatcdf) structure.

### -param pPrevAttr [in]

A pointer to a [CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute) structure for a catalog attribute in the CDF pointed to by <i>pCDF</i>.

### -param pfnParseError [in]

A pointer to a user-defined function to handle file parse errors.

## -returns

Upon success, this function returns a pointer to a [CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute) structure. The <b>CryptCATCDFEnumCatAttributes</b> function returns a <b>NULL</b> pointer if it fails.

## -remarks

You typically call this function in a loop to enumerate all of the catalog header attributes in a CDF. Before entering the loop, set <i>pPrevAttr</i> to <b>NULL</b>. The function returns a pointer to the first attribute. Set <i>pPrevAttr</i> to the return  value of the function for subsequent iterations of the loop.


#### Examples

The following example shows the correct sequence of assignments for the <i>pPrevAttr</i> parameter (<code>pAttr</code>).


```cpp
    CRYPTCATCDF         *pCDF;
    CRYPTCATATTRIBUTE   *pAttr;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    
    pAttr = NULL;

    while (pAttr = CryptCATCDFEnumCatAttributes(pCDF, pAttr, NULL))
    {
        //do something with pAttr
    }

    CryptCATCDFClose(pCDF);

```

## -see-also

[CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute)



[CRYPTCATCDF](/windows/desktop/api/mscat/ns-mscat-cryptcatcdf)



<a href="/windows/desktop/SecCrypto/makecat">MakeCat</a>