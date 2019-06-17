---
UID: NF:adshlp.AllocADsStr
title: AllocADsStr function (adshlp.h)
author: windows-sdk-content
description: Allocates memory for and copies a specified string.
old-location: adsi\allocadsstr.htm
tech.root: adsi
ms.assetid: 1e2b6d42-a879-4a53-a2ce-0e841f6b8543
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AllocADsStr, AllocADsStr function [ADSI], _ds_allocadsstr, adshlp/AllocADsStr, adsi.allocadsstr
ms.topic: function
f1_keywords: ["adshlp/AllocADsStr"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - AllocADsStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AllocADsStr function


## -description


The <b>AllocADsStr</b> function allocates memory for and copies a specified string.


## -parameters




### -param pStr [in]

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string to be copied.


## -returns



Type: <b>LPWSTR</b>

When successful, the function returns a non-<b>NULL</b> pointer to the allocated memory. The string in <i>pStr</i> is copied to this buffer and null-terminated. The caller must  free this memory when it is no longer required by passing the returned pointer to <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-freeadsstr">FreeADsStr</a>.

Returns <b>NULL</b> if not successful. Call  <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">ADsGetLastError</a> to obtain the extended error status. For more information about error code values, see  <a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.




## -remarks



For more information and a code example that shows how to use the <b>AllocADsStr</b> function, see <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">ADsGetLastError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-freeadsstr">FreeADsStr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a>
 

 

