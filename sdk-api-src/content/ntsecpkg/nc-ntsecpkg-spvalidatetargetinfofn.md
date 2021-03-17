---
UID: NC:ntsecpkg.SpValidateTargetInfoFn
title: SpValidateTargetInfoFn (ntsecpkg.h)
description: Validates that the specified SECPKG_TARGETINFO structure represents a valid target.
helpviewer_keywords: ["SpValidateTargetInfoFn","SpValidateTargetInfoFn callback","SpValidateTargetInfoFn callback function [Security]","ntsecpkg/SpValidateTargetInfoFn","security.spvalidatetargetinfofn"]
old-location: security\spvalidatetargetinfofn.htm
tech.root: security
ms.assetid: 01d1b74a-14d9-40cd-bcca-a031f5fc9cbb
ms.date: 12/05/2018
ms.keywords: SpValidateTargetInfoFn, SpValidateTargetInfoFn callback, SpValidateTargetInfoFn callback function [Security], ntsecpkg/SpValidateTargetInfoFn, security.spvalidatetargetinfofn
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - SpValidateTargetInfoFn
 - ntsecpkg/SpValidateTargetInfoFn
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
 - SpValidateTargetInfoFn
---

# SpValidateTargetInfoFn callback function


## -description

Validates that the specified <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_targetinfo">SECPKG_TARGETINFO</a> structure represents a valid target.

## -parameters

### -param ClientRequest [in, optional]

A pointer to an opaque 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> data structure that contains information about the LSA client's authentication request. A custom authentication package should pass in the value received during the client's call to the function, such as 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_call_package">LsaApCallPackage</a> or 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a>, that returns the output parameter.

### -param ProtocolSubmitBuffer [in]

A pointer to the input buffer sent by the client.

### -param ClientBufferBase [in]

The base address of the input buffer, in the client's address space.

### -param SubmitBufferLength [in]

The size, in bytes, of the <i>ProtocolSubmitBuffer</i> buffer.

### -param TargetInfo [in]

A pointer to a <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_targetinfo">SECPKG_TARGETINFO</a> structure that specifies the target to validate.

## -returns

If the function succeeds and the specified target is a valid target, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

SSP/APs must implement the <b>SpValidateTargetInfo</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpValidateTargetInfo</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>