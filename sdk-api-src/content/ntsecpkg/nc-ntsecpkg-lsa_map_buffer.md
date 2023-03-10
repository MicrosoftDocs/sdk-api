---
UID: NC:ntsecpkg.LSA_MAP_BUFFER
title: LSA_MAP_BUFFER (ntsecpkg.h)
description: Maps a SecBuffer structure into the address space of the security support provider/authentication package (SSP/AP).
helpviewer_keywords: ["LSA_MAP_BUFFER","LSA_MAP_BUFFER callback","MapBuffer","MapBuffer callback function [Security]","_ssp_mapbuffer","ntsecpkg/MapBuffer","security.mapbuffer"]
old-location: security\mapbuffer.htm
tech.root: security
ms.assetid: 3189da1b-5f2f-4569-8f60-6f3b287460f1
ms.date: 12/05/2018
ms.keywords: LSA_MAP_BUFFER, LSA_MAP_BUFFER callback, MapBuffer, MapBuffer callback function [Security], _ssp_mapbuffer, ntsecpkg/MapBuffer, security.mapbuffer
req.header: ntsecpkg.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_MAP_BUFFER
 - ntsecpkg/LSA_MAP_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - MapBuffer
---

# LSA_MAP_BUFFER callback function


## -description

The <b>MapBuffer</b> function maps a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure into the address space of the <a href="/windows/desktop/SecGloss/s-gly">security support provider</a>/<a href="/windows/desktop/SecGloss/a-gly">authentication package</a> (SSP/AP).

## -parameters

### -param InputBuffer [in]

Pointer to the 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure to map.

### -param OutputBuffer [out]

Pointer that receives the address of the mapped 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.

## -remarks

If the 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> has already been mapped, the <b>MapBuffer</b> function copies the contents of the input buffer over the output buffer.

A pointer to the <b>MapBuffer</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>