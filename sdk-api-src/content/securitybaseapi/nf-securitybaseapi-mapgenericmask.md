---
UID: NF:securitybaseapi.MapGenericMask
title: MapGenericMask function (securitybaseapi.h)
description: Maps the generic access rights in an access mask to specific and standard access rights. The function applies a mapping supplied in a GENERIC_MAPPING structure.
helpviewer_keywords: ["MapGenericMask","MapGenericMask function [Security]","_win32_mapgenericmask","security.mapgenericmask","securitybaseapi/MapGenericMask"]
old-location: security\mapgenericmask.htm
tech.root: security
ms.assetid: 54b5cd73-4011-4dcf-a951-7350dbd6eeab
ms.date: 12/05/2018
ms.keywords: MapGenericMask, MapGenericMask function [Security], _win32_mapgenericmask, security.mapgenericmask, securitybaseapi/MapGenericMask
req.header: securitybaseapi.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapGenericMask
 - securitybaseapi/MapGenericMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - MapGenericMask
---

# MapGenericMask function


## -description

The <b>MapGenericMask</b> function maps the generic access rights in an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> to specific and standard access rights. The function applies a mapping supplied in a 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure.

## -parameters

### -param AccessMask [in, out]

A pointer to an access mask.

### -param GenericMapping [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure specifying a mapping of generic access types to specific and standard access types.

## -remarks

After calling the <b>MapGenericMask</b> function, the access mask pointed to by the <i>AccessMask</i> parameter has none of its generic bits (GenericRead, GenericWrite, GenericExecute, or GenericAll) or undefined bits set, although it can have other bits set. If bits other than the generic bits are provided on input, this function does not clear them.


#### Examples

For an example that uses this function, see 
     <a href="/windows/desktop/SecAuthZ/verifying-client-access-with-acls-in-c--">Verifying Client Access with ACLs</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted">AreAllAccessesGranted</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted">AreAnyAccessesGranted</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>