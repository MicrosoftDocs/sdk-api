---
UID: NF:adshlp.FreeADsStr
title: FreeADsStr function (adshlp.h)
description: Frees the memory of a string allocated by AllocADsStr or ReallocADsStr.
helpviewer_keywords: ["FreeADsStr","FreeADsStr function [ADSI]","_ds_freeadsstr","adshlp/FreeADsStr","adsi.freeadsstr"]
old-location: adsi\freeadsstr.htm
tech.root: adsi
ms.assetid: 9c8eaac2-1fb4-47f9-8f60-6896073012aa
ms.date: 12/05/2018
ms.keywords: FreeADsStr, FreeADsStr function [ADSI], _ds_freeadsstr, adshlp/FreeADsStr, adsi.freeadsstr
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeADsStr
 - adshlp/FreeADsStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
 - AdsLdpc.dll
api_name:
 - FreeADsStr
---

# FreeADsStr function


## -description

The <b>FreeADsStr</b> function frees the memory of a 
   string allocated by  <a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a> or 
   <a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a>.

## -parameters

### -param pStr [in]

Type: <b>LPWSTR</b>

Pointer to the string to be freed. This string must have been allocated with the 
      <a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a> or 
      <a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a> function.

## -returns

Type: <b>BOOL</b>

The function returns <b>TRUE</b> if the memory is freed. Otherwise, it returns 
      <b>FALSE</b>.

## -remarks

Do not use this function to free memory allocated with the 
    <a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a> or 
    <a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a> function. Use the 
    <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a> function  to free memory allocated with these 
    functions.

For more information and a code example that shows how to use the 
    <b>FreeADsStr</b> function, see 
    <a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a>