---
UID: NC:ntsecpkg.LSA_CLOSE_SAM_USER
title: LSA_CLOSE_SAM_USER (ntsecpkg.h)
description: Closes a handle to a Security Accounts Manager (SAM) user account.
helpviewer_keywords: ["CloseSamUser","CloseSamUser callback function [Security]","LSA_CLOSE_SAM_USER","LSA_CLOSE_SAM_USER callback","_ssp_closesamuser","ntsecpkg/CloseSamUser","security.closesamuser"]
old-location: security\closesamuser.htm
tech.root: security
ms.assetid: 1e56e38e-ba8f-4781-80f1-e60bd33250e4
ms.date: 12/05/2018
ms.keywords: CloseSamUser, CloseSamUser callback function [Security], LSA_CLOSE_SAM_USER, LSA_CLOSE_SAM_USER callback, _ssp_closesamuser, ntsecpkg/CloseSamUser, security.closesamuser
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
 - LSA_CLOSE_SAM_USER
 - ntsecpkg/LSA_CLOSE_SAM_USER
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
 - CloseSamUser
---

# LSA_CLOSE_SAM_USER callback function


## -description

The <b>CloseSamUser</b> function closes a handle to a Security Accounts Manager (SAM) user account.

## -parameters

### -param UserHandle [in]

A handle to the SAM user account previously opened using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a> function.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason. The following table lists a common reason for failure and the error code that the function returns.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified for <i>UserHandle</i> is not valid or <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

A pointer to the <b>CloseSamUser</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>