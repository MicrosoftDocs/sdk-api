---
UID: NF:authz.AuthzModifySids
title: AuthzModifySids function (authz.h)
description: Adds, deletes, or modifies user and device groups in the Authz client context.
helpviewer_keywords: ["AuthzModifySids","AuthzModifySids function [Security]","authz/AuthzModifySids","security.authzmodifysids"]
old-location: security\authzmodifysids.htm
tech.root: security
ms.assetid: 740569A5-6159-409B-B8CB-B3A8BAE4F398
ms.date: 12/05/2018
ms.keywords: AuthzModifySids, AuthzModifySids function [Security], authz/AuthzModifySids, security.authzmodifysids
req.header: authz.h
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuthzModifySids
 - authz/AuthzModifySids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzModifySids
---

# AuthzModifySids function


## -description

The <b>AuthzModifySids</b> function adds, deletes, or modifies user and device groups in the Authz client context.

## -parameters

### -param hAuthzClientContext [in]

A handle to the client context to be modified.

### -param SidClass [in]

Type of information to be modified. The caller can specify AuthzContextInfoGroupsSids, AuthzContextInfoRestrictedSids, or AuthzContextInfoDeviceSids.

### -param pSidOperations [in]

A pointer to an array of <a href="/windows/desktop/api/authz/ne-authz-authz_sid_operation">AUTHZ_SID_OPERATION</a> enumeration values that specify the group modifications to make.

### -param pSids [in, optional]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that specifies the groups to modify.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/authz/ne-authz-authz_sid_operation">AUTHZ_SID_OPERATION</a> enumeration must have only one element if the value of that element is AUTHZ_SID_OPERATION_REPLACE_ALL. Otherwise, the array has the same number of elements as the corresponding 
PTOKEN_GROUPS.


When you want to use <b>AuthzModifySids</b> to delete, the SIDs are matched but not the SID flags. If no matching SID is found, no modifications are done and the call fails.