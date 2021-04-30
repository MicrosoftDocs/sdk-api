---
UID: NC:ntsecpkg.LSA_CALL_PACKAGE
title: LSA_CALL_PACKAGE (ntsecpkg.h)
description: The CallPackage function is used to call another security package to access its services.
helpviewer_keywords: ["CallPackage","CallPackage callback function [Security]","LSA_CALL_PACKAGE","LSA_CALL_PACKAGE callback","_ssp_callpackage","ntsecpkg/CallPackage","security.callpackage"]
old-location: security\callpackage.htm
tech.root: security
ms.assetid: 770c41ab-df79-4371-9f1d-7bbce8193b5d
ms.date: 12/05/2018
ms.keywords: CallPackage, CallPackage callback function [Security], LSA_CALL_PACKAGE, LSA_CALL_PACKAGE callback, _ssp_callpackage, ntsecpkg/CallPackage, security.callpackage
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
 - LSA_CALL_PACKAGE
 - ntsecpkg/LSA_CALL_PACKAGE
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
 - CallPackage
---

# LSA_CALL_PACKAGE callback function


## -description

The <b>CallPackage</b> function is used to call another <a href="/windows/desktop/SecGloss/s-gly">security package</a> to access its services.

## -parameters

### -param AuthenticationPackage [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the package to call.

### -param ProtocolSubmitBuffer [in]

Pointer to the input buffer. The content of this buffer is package-specific.

### -param SubmitBufferLength [in]

Size of the <i>ProtocolSubmitBuffer</i> parameter in bytes.

### -param ProtocolReturnBuffer [out]

Pointer that receives the address of the output buffer. The content of this buffer is package-specific.

### -param ReturnBufferLength [out]

Pointer to a variable that receives the size of the <i>ProtocolReturnBuffer</i> parameter in bytes.

### -param ProtocolStatus [out]

Pointer to a variable that receives the status code returned by the called package.

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
The <i>AuthenticationPackage</i> parameter does not contain the name of a valid <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

</td>
</tr>
</table>

## -remarks

A pointer to the <b>CallPackage</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_call_packageex">CallPackageEx</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
