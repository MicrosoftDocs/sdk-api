---
UID: NF:adshlp.AllocADsMem
title: AllocADsMem function (adshlp.h)
description: Allocates a block of memory of the specified size.
helpviewer_keywords: ["AllocADsMem","AllocADsMem function [ADSI]","_ds_allocadsmem","adshlp/AllocADsMem","adsi.allocadsmem"]
old-location: adsi\allocadsmem.htm
tech.root: adsi
ms.assetid: df98a728-596b-4541-974a-5690e510ad9f
ms.date: 12/05/2018
ms.keywords: AllocADsMem, AllocADsMem function [ADSI], _ds_allocadsmem, adshlp/AllocADsMem, adsi.allocadsmem
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
 - AllocADsMem
 - adshlp/AllocADsMem
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
 - AllocADsMem
---

# AllocADsMem function


## -description

The <b>AllocADsMem</b> function allocates a block of memory of the specified size.

## -parameters

### -param cb [in]

Type: <b>DWORD</b>

Contains the size, in bytes, to be allocated.

## -returns

Type: <b>LPVOID</b>

When successful, the function returns a non-<b>NULL</b> pointer to the allocated memory. The caller must free this memory when it is no longer required by passing the returned pointer to <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>.

Returns <b>NULL</b> if not successful. Call  <a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">ADsGetLastError</a> to obtain extended error status. For more information about error code values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The memory block returned by <b>AllocADsMem</b> is initialized to zero.

For more information and a code example that shows how to use the <b>AllocADsMem</b> function, see <a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">ADsGetLastError</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>