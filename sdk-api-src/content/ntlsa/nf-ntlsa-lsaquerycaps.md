---
UID: NF:ntlsa.LsaQueryCAPs
title: LsaQueryCAPs function (ntlsa.h)
description: Returns the Central Access Policies (CAPs) for the specified IDs.
helpviewer_keywords: ["LsaQueryCAPs","LsaQueryCAPs function [Security]","ntlsa/LsaQueryCAPs","security.lsaquerycaps"]
old-location: security\lsaquerycaps.htm
tech.root: security
ms.assetid: 55D6FD6F-0FD5-41F6-967B-F5600E19C3EF
ms.date: 12/05/2018
ms.keywords: LsaQueryCAPs, LsaQueryCAPs function [Security], ntlsa/LsaQueryCAPs, security.lsaquerycaps
req.header: ntlsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - LsaQueryCAPs
 - ntlsa/LsaQueryCAPs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - LsaQueryCAPs
---

# LsaQueryCAPs function


## -description

Returns the Central Access Policies (CAPs) for the specified IDs.

## -parameters

### -param CAPIDs

A pointer to a variable that contains an array of pointers to CAPIDs that identify the CAPs being queried.

### -param CAPIDCount [in]

The number of IDs in the <i>CAPIDs</i> parameter.

### -param CAPs [out]

Receives a pointer to an array of pointers to <a href="/windows/desktop/api/ntlsa/ns-ntlsa-central_access_policy">CENTRAL_ACCESS_POLICY</a> structures representing the queried CAPs.

### -param CAPCount [out]

The number of <a href="/windows/desktop/api/ntlsa/ns-ntlsa-central_access_policy">CENTRAL_ACCESS_POLICY</a> structure pointers returned in the <i>CAPs</i> parameter.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the <a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.