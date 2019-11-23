---
UID: NF:adshlp.FreeADsMem
title: FreeADsMem function (adshlp.h)

description: Frees the memory allocated by AllocADsMem or ReallocADsMem.
old-location: adsi\freeadsmem.htm
tech.root: adsi
ms.assetid: e43f050a-5b96-406e-87ed-88a39ea747da

ms.date: 12/05/2018
ms.keywords: FreeADsMem, FreeADsMem function [ADSI], _ds_freeadsmem, adshlp/FreeADsMem, adsi.freeadsmem
ms.topic: function
f1_keywords: 
 - "adshlp/FreeADsMem"
dev_langs:
 - c++
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll; AdsLdpc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
 - AdsLdpc.dll
api_name:
 - FreeADsMem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FreeADsMem function


## -description


The <b>FreeADsMem</b> function frees the memory allocated by  <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a> or <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>.


## -parameters




### -param pMem [in]

Type: <b>LPVOID</b>

Pointer to the memory to be freed. This memory must have been allocated with the <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a> or <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a> function.


## -returns



Type: <b>BOOL</b>

The function returns <b>TRUE</b> if successful, otherwise it returns <b>FALSE</b>.




## -remarks



Do not use this  function to free memory allocated with the <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a> or <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a> function. Use the  <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-freeadsstr">FreeADsStr</a> function to free memory allocated with these functions.

For more information and  a code example that shows how to use the <b>FreeADsMem</b> function, see <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-freeadsstr">FreeADsStr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a>
 

 

