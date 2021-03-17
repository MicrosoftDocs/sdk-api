---
UID: NF:adshlp.ReallocADsStr
title: ReallocADsStr function (adshlp.h)
description: Creates a copy of a Unicode string.
helpviewer_keywords: ["ReallocADsStr","ReallocADsStr function [ADSI]","_ds_reallocadsstr","adshlp/ReallocADsStr","adsi.reallocadsstr"]
old-location: adsi\reallocadsstr.htm
tech.root: adsi
ms.assetid: 805d45dc-8da4-4c15-a6d1-8967a4da9c24
ms.date: 12/05/2018
ms.keywords: ReallocADsStr, ReallocADsStr function [ADSI], _ds_reallocadsstr, adshlp/ReallocADsStr, adsi.reallocadsstr
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReallocADsStr
 - adshlp/ReallocADsStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ReallocADsStr
---

# ReallocADsStr function


## -description

The <b>ReallocADsStr</b> function creates a copy of a Unicode string.

## -parameters

### -param ppStr [out]

Type: <b>LPWSTR*</b>

Pointer to null-terminated Unicode string pointer that receives the allocated string. <b>ReallocADsStr</b> will attempt to free this memory with <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsstr">FreeADsStr</a> before reallocating the string, so this parameter should be initialized to <b>NULL</b> if the memory should not be freed or was not allocated with the <a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a>, <a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a>, <a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a> or <b>ReallocADsStr</b> function.

The caller must free this memory when it is no longer required by passing this pointer to <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsstr">FreeADsStr</a>.

### -param pStr [in]

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string that contains the string to copy.

## -returns

Type: <b>BOOL</b>

The function returns <b>TRUE</b> if  successful, otherwise <b>FALSE</b> is returned.

## -see-also

<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsstr">FreeADsStr</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>