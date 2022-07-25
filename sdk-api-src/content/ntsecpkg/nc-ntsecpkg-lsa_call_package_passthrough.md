---
UID: NC:ntsecpkg.LSA_CALL_PACKAGE_PASSTHROUGH
title: LSA_CALL_PACKAGE_PASSTHROUGH (ntsecpkg.h)
description: The CallPackagePassthrough function is used to call another security package to access its services.
helpviewer_keywords: ["CallPackagePassthrough","CallPackagePassthrough callback function [Security]","LSA_CALL_PACKAGE_PASSTHROUGH","LSA_CALL_PACKAGE_PASSTHROUGH callback","_ssp_callpackagepassthrough","ntsecpkg/CallPackagePassthrough","security.callpackagepassthrough"]
old-location: security\callpackagepassthrough.htm
tech.root: security
ms.assetid: 622856ca-f49e-4995-bead-7b02501a84e5
ms.date: 12/05/2018
ms.keywords: CallPackagePassthrough, CallPackagePassthrough callback function [Security], LSA_CALL_PACKAGE_PASSTHROUGH, LSA_CALL_PACKAGE_PASSTHROUGH callback, _ssp_callpackagepassthrough, ntsecpkg/CallPackagePassthrough, security.callpackagepassthrough
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
 - LSA_CALL_PACKAGE_PASSTHROUGH
 - ntsecpkg/LSA_CALL_PACKAGE_PASSTHROUGH
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
 - CallPackagePassthrough
---

# LSA_CALL_PACKAGE_PASSTHROUGH callback function


## -description

The <b>CallPackagePassthrough</b> function is used to call another <a href="/windows/desktop/SecGloss/s-gly">security package</a> to access its services.

## -parameters

### -param AuthenticationPackage [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the package to call.

### -param ClientBufferBase [in]

The base address of the input buffer, in the client's address space.

### -param ProtocolSubmitBuffer [in]

Pointer to the input buffer.

### -param SubmitBufferLength [in]

Size of the <i>ProtocolSubmitBuffer</i> parameter in bytes.

### -param ProtocolReturnBuffer [out]

Pointer to the output buffer.

### -param ReturnBufferLength [out]

Pointer to a variable that receives the size of the <i>ProtocolReturnBuffer</i> parameter in bytes.

### -param ProtocolStatus [out]

Pointer to a variable that receives the status code returned by the package.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed. The following table lists a common reason for failure and the error code that the function returns.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>AuthenticationPackage</i> parameter does not contain the name of a valid SSP/AP.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) does not examine or alter any of the function arguments.

A pointer to the <b>CallPackagePassthrough</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_package">CallPackage</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_packageex">CallPackageEx</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
