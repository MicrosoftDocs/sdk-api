---
UID: NF:userenv.RsopFileAccessCheck
title: RsopFileAccessCheck function (userenv.h)
description: The RSoPFileAccessCheck function determines whether a file's security descriptor grants a specified set of file access rights to the client identified by an RSOPTOKEN.
helpviewer_keywords: ["RSoPFileAccessCheck","RSoPFileAccessCheck function [Group Policy]","RsopFileAccessCheck","_win32_rsopfileaccesscheck","policy.rsopfileaccesscheck","userenv/RSoPFileAccessCheck"]
old-location: policy\rsopfileaccesscheck.htm
tech.root: Policy
ms.assetid: dfdf14ee-fee1-4e96-9955-7f24dfe39487
ms.date: 12/05/2018
ms.keywords: RSoPFileAccessCheck, RSoPFileAccessCheck function [Group Policy], RsopFileAccessCheck, _win32_rsopfileaccesscheck, policy.rsopfileaccesscheck, userenv/RSoPFileAccessCheck
req.header: userenv.h
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
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RsopFileAccessCheck
 - userenv/RsopFileAccessCheck
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - RSoPFileAccessCheck
---

# RsopFileAccessCheck function


## -description

The
    <b>RSoPFileAccessCheck</b> function determines whether a file's security descriptor grants a specified set of file access rights to the client identified by an <b>RSOPTOKEN</b>.

## -parameters

### -param pszFileName [in]

Pointer to the name of the relevant file. The file must already exist.

### -param pRsopToken [in]

Pointer to a valid <b>RSOPTOKEN</b> representing the client attempting to gain access to the file.

### -param dwDesiredAccessMask [in]

Specifies an access mask that indicates the access rights to check. This mask can contain a combination of 
<a href="/windows/desktop/SecAuthZ/generic-access-rights">generic</a>, 
<a href="/windows/desktop/SecAuthZ/standard-access-rights">standard</a>, and specific access rights. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-and-access-masks">Access Rights and Access Masks</a>.

### -param pdwGrantedAccessMask [out]

Pointer to an access mask that receives the granted access rights.

If the function succeeds, the <i>pbAccessStatus</i> parameter is set to <b>TRUE</b>, and the mask is updated to contain the standard and specific rights granted. If <i>pbAccessStatus</i> is set to <b>FALSE</b>, this parameter is set to zero. If the function fails, the mask is not modified.

### -param pbAccessStatus [out]

Pointer to a variable that receives the results of the access check.

If the function succeeds, and the requested set of access rights are granted, this parameter is set to <b>TRUE</b>. Otherwise, this parameter is set to <b>FALSE</b>. If the function fails, the status is not modified.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

The 
<b>RSoPFileAccessCheck</b> function indicates, in the <i>pbAccessStatus</i> parameter, whether access is granted or denied to the client identified by the <b>RSOPTOKEN</b>. If access is granted, the requested access mask becomes the object's granted access mask.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nf-userenv-rsopaccesscheckbytype">RSoPAccessCheckByType</a>