---
UID: NF:mscat.CryptCATCDFEnumCatAttributes
title: CryptCATCDFEnumCatAttributes function (mscat.h)
author: windows-sdk-content
description: Enumerates catalog-level attributes within the CatalogHeader section of a catalog definition file (CDF).
old-location: security\cryptcatcdfenumcatattributes.htm
tech.root: SecCrypto
ms.assetid: 01889cb9-7bf4-4591-9bb2-b263c4effe0c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptCATCDFEnumCatAttributes, CryptCATCDFEnumCatAttributes function [Security], mscat/CryptCATCDFEnumCatAttributes, security.cryptcatcdfenumcatattributes
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATCDFEnumCatAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATCDFEnumCatAttributes function


## -description


<p class="CCE_Message">[The  <b>CryptCATCDFEnumCatAttributes</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATCDFEnumCatAttributes</b> function enumerates catalog-level attributes within the <b>CatalogHeader</b> section of a catalog definition file (CDF). <b>CryptCATCDFEnumCatAttributes</b> is called by <a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a>.


## -parameters




### -param pCDF [in]

A pointer to a <a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a> structure.


### -param pPrevAttr [in]

A pointer to a <a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a> structure for a catalog attribute in the CDF pointed to by <i>pCDF</i>.


### -param pfnParseError [in]

A pointer to a user-defined function to handle file parse errors.


## -returns



Upon success, this function returns a pointer to a <a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a> structure. The <b>CryptCATCDFEnumCatAttributes</b> function returns a <b>NULL</b> pointer if it fails.




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




<a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a>



<a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a>



<a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a>
 

 

