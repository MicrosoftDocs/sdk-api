---
UID: NF:authz.AuthzModifySecurityAttributes
title: AuthzModifySecurityAttributes function (authz.h)
description: Modifies the security attribute information in the specified client context.helpviewer_keywords: ["AuthzModifySecurityAttributes","AuthzModifySecurityAttributes function [Security]","authz/AuthzModifySecurityAttributes","security.authzmodifysecurityattributes"]
old-location: security\authzmodifysecurityattributes.htm
tech.root: SecAuthZ
ms.assetid: d84873e2-ecfe-45cf-9048-7ed173117efa
ms.date: 12/05/2018
ms.keywords: AuthzModifySecurityAttributes, AuthzModifySecurityAttributes function [Security], authz/AuthzModifySecurityAttributes, security.authzmodifysecurityattributes
f1_keywords:
- authz/AuthzModifySecurityAttributes
dev_langs:
- c++
req.header: authz.h
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Authz.dll
api_name:
- AuthzModifySecurityAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuthzModifySecurityAttributes function


## -description


The <b>AuthzModifySecurityAttributes</b> function modifies the security attribute information in the specified client context.


## -parameters




### -param hAuthzClientContext [in]

A handle to the client context to be modified.


### -param pOperations [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/authz/ne-authz-authz_security_attribute_operation">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration values that specify the types of modifications to make.

This array must have only one element if the value of that element is <b>AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL</b>. Otherwise, the array has the same number of elements as the <i>pAttributes</i> array.


### -param pAttributes [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that specifies the attributes to modify.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



