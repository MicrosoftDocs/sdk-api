---
UID: NF:securitybaseapi.DeriveCapabilitySidsFromName
title: DeriveCapabilitySidsFromName function (securitybaseapi.h)
description: This function constructs two arrays of SIDs out of a capability name. One is an array group SID with NT Authority, and the other is an array of capability SIDs with AppAuthority.
helpviewer_keywords: ["DeriveCapabilitySidsFromName","DeriveCapabilitySidsFromName function [Security]","security.derivecapabilitysidsfromname","securitybaseapi/DeriveCapabilitySidsFromName"]
old-location: security\derivecapabilitysidsfromname.htm
tech.root: security
ms.assetid: 1A911FCC-6D11-4185-B532-20FE6C7C4B0B
ms.date: 03/20/2025
ms.keywords: DeriveCapabilitySidsFromName, DeriveCapabilitySidsFromName function [Security], security.derivecapabilitysidsfromname, securitybaseapi/DeriveCapabilitySidsFromName
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCoreUAP.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeriveCapabilitySidsFromName
 - securitybaseapi/DeriveCapabilitySidsFromName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Kernel32.dll
api_name:
 - DeriveCapabilitySidsFromName
---

# DeriveCapabilitySidsFromName function


## -description

This function constructs two arrays of SIDs out of a capability name. One is an array group SID with NT Authority, and the other is an array of capability SIDs with AppAuthority.

## -parameters

### -param CapName [in]

Name of the capability in string form.

### -param CapabilityGroupSids [out]

The GroupSids with NTAuthority.

### -param CapabilityGroupSidCount [out]

The count of GroupSids in the array.

### -param CapabilitySids [out]

CapabilitySids with AppAuthority.

### -param CapabilitySidCount [out]

The count of CapabilitySid with AppAuthority.

## -returns

If the function succeeds, it returns **TRUE**.

If the function fails, it returns **FALSE**. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The caller is expected to free the individual SIDs returned in each array by calling `LocalFree`, as well as memory allocated for the array itself.

The SID computed for the application capability of legacy capabilities (published prior to Win10) will be the same as the published SIDs but the SID for the service group capability SID will be hash based.