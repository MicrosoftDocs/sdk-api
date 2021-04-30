---
UID: NC:ntsecpkg.SpMarshallSupplementalCredsFn
title: SpMarshallSupplementalCredsFn (ntsecpkg.h)
description: Converts supplemental credentials from a public format into a format suitable for local procedure calls.
helpviewer_keywords: ["SpMarshallSupplementalCreds","SpMarshallSupplementalCreds callback function [Security]","SpMarshallSupplementalCredsFn","SpMarshallSupplementalCredsFn callback","_ssp_spmarshallsupplementalcreds","ntsecpkg/SpMarshallSupplementalCreds","security.spmarshallsupplementalcreds"]
old-location: security\spmarshallsupplementalcreds.htm
tech.root: security
ms.assetid: 64792843-5129-4a71-b88b-b4caf495a567
ms.date: 12/05/2018
ms.keywords: SpMarshallSupplementalCreds, SpMarshallSupplementalCreds callback function [Security], SpMarshallSupplementalCredsFn, SpMarshallSupplementalCredsFn callback, _ssp_spmarshallsupplementalcreds, ntsecpkg/SpMarshallSupplementalCreds, security.spmarshallsupplementalcreds
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
 - SpMarshallSupplementalCredsFn
 - ntsecpkg/SpMarshallSupplementalCredsFn
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
 - SpMarshallSupplementalCreds
---

# SpMarshallSupplementalCredsFn callback function


## -description

The <b>SpMarshallSupplementalCreds</b> function converts <a href="/windows/desktop/SecGloss/s-gly">supplemental credentials</a> from a public format into a format suitable for local procedure calls.

## -parameters

### -param CredentialSize [in]

Specifies the size of the supplemental credentials.

### -param Credentials [in]

Pointer to the supplemental credentials.

### -param MarshalledCredSize [out]

Pointer to the size of the <i>MarshalledCreds</i> buffer.

### -param MarshalledCreds [out]

Pointer that receives the address of the buffer containing the <a href="/windows/desktop/SecGloss/s-gly">serialized</a> credentials. Allocate the memory for this buffer by calling the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateHeap</a> function.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

SSP/APs must implement the <b>SpMarshallSupplementalCreds</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpMarshallSupplementalCreds</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)">AllocateHeap</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>
