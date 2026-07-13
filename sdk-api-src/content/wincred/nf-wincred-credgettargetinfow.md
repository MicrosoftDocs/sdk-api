---
UID: NF:wincred.CredGetTargetInfoW
title: CredGetTargetInfoW function (wincred.h)
description: The CredGetTargetInfo function retrieves all known target name information for the named target computer. (Unicode)
helpviewer_keywords: ["CredGetTargetInfo", "CredGetTargetInfo function [Security]", "CredGetTargetInfoW", "_cred_credgettargetinfo", "security.credgettargetinfo", "wincred/CredGetTargetInfo", "wincred/CredGetTargetInfoW"]
old-location: security\credgettargetinfo.htm
tech.root: security
ms.assetid: 14dca0af-72d7-4ca8-84bb-c7040c5b5fb9
ms.date: 12/05/2018
ms.keywords: CredGetTargetInfo, CredGetTargetInfo function [Security], CredGetTargetInfoA, CredGetTargetInfoW, _cred_credgettargetinfo, security.credgettargetinfo, wincred/CredGetTargetInfo, wincred/CredGetTargetInfoA, wincred/CredGetTargetInfoW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredGetTargetInfoW (Unicode) and CredGetTargetInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredGetTargetInfoW
 - wincred/CredGetTargetInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredGetTargetInfo
 - CredGetTargetInfoA
 - CredGetTargetInfoW
---

# CredGetTargetInfoW function


## -description

The <b>CredGetTargetInfo</b> function retrieves all known target name information for the named target computer. This executed locally and does not need any particular privilege. The information returned is expected to be passed to the 
<a href="/windows/desktop/api/wincred/nf-wincred-credreaddomaincredentialsa">CredReadDomainCredentials</a> and 
<a href="/windows/desktop/api/wincred/nf-wincred-credwritedomaincredentialsa">CredWriteDomainCredentials</a> functions. The information should not be used for any other purpose.

Authentication packages compute <i>TargetInfo</i> when attempting to authenticate to a <i>TargetName</i>. The authentication packages cache this target information to make it available to <b>CredGetTargetInfo</b>. Therefore, the target information will only be available from a recent attempt to authenticate a <i>TargetName</i>.

Authentication packages not in the LSA process can cache a <i>TargetInfo</i> for later retrieval by <b>CredGetTargetInfo</b> by calling <a href="/windows/desktop/api/wincred/nf-wincred-credreaddomaincredentialsa">CredReadDomainCredentials</a> with the CRED_CACHE_TARGET_INFORMATION flag.

## -parameters

### -param TargetName [in]

Pointer to a null-terminated string that contains the name of the target computer for which information is to be retrieved.

### -param Flags [in]

Flags controlling the operation of the function. The following flag can be used: 




CRED_ALLOW_NAME_RESOLUTION

If no target information can be found for <i>TargetName</i> name resolution is done on <i>TargetName</i> to convert it to other forms. If target information exists for any of those other forms, it is returned. Currently only DNS name resolution is done.

This is useful if the application does not call an authentication package directly. The application can pass the <i>TargetName</i> to another layer of software to authenticate to the server, and that layer of software might resolve the name and pass the resolved name to the authentication package. As such, there will be no target information for the original <i>TargetName</i>.

### -param TargetInfo [out]

Pointer to a single allocated block buffer to contain the target information. At least one of the returned members of <i>TargetInfo</i> will be non-NULL. Any pointers contained within the buffer are pointers to locations within this single allocated block. The single returned buffer must be freed by calling <a href="/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>.

## -returns

The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

<ul>
<li>ERROR_NOT_FOUND 


Target information for the named server is not available.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>



<a href="/windows/desktop/api/wincred/nf-wincred-credreaddomaincredentialsa">CredReadDomainCredentials</a>



<a href="/windows/desktop/api/wincred/nf-wincred-credwritedomaincredentialsa">CredWriteDomainCredentials</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>

## -remarks

> [!NOTE]
> The wincred.h header defines CredGetTargetInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
