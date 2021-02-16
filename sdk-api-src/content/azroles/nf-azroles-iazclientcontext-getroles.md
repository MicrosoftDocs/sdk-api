---
UID: NF:azroles.IAzClientContext.GetRoles
title: IAzClientContext::GetRoles (azroles.h)
description: Returns the roles for the client context.
helpviewer_keywords: ["AzClientContext object [Security]","GetRoles method","GetRoles","GetRoles method [Security]","GetRoles method [Security]","AzClientContext object","GetRoles method [Security]","IAzClientContext interface","IAzClientContext interface [Security]","GetRoles method","IAzClientContext.GetRoles","IAzClientContext::GetRoles","azroles/IAzClientContext::GetRoles","security.iazclientcontext_getroles"]
old-location: security\iazclientcontext_getroles.htm
tech.root: security
ms.assetid: 753506cc-ed44-4795-90e5-c76010181d8a
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],GetRoles method, GetRoles, GetRoles method [Security], GetRoles method [Security],AzClientContext object, GetRoles method [Security],IAzClientContext interface, IAzClientContext interface [Security],GetRoles method, IAzClientContext.GetRoles, IAzClientContext::GetRoles, azroles/IAzClientContext::GetRoles, security.iazclientcontext_getroles
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzClientContext::GetRoles
 - azroles/IAzClientContext::GetRoles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext.GetRoles
 - AzClientContext.GetRoles
---

# IAzClientContext::GetRoles


## -description

The <b>GetRoles</b> method returns the roles for the client context.

## -parameters

### -param bstrScopeName [in, optional]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object from which the roles returned in the <i>pvarRoleNames</i> parameter are applicable. If this property is <b>NULL</b>, the roles from the application scope are returned; otherwise, the roles from the specified scope are returned instead of the roles from the application scope.

### -param pvarRoleNames [out]

A pointer to a <b>VARIANT</b> used to return a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>. Each element of the <b>SAFEARRAY</b> is a <b>VARIANT</b> of type <b>BSTR</b> that contains the name of a role to which the client belongs at the scope specified by the <i>bstrScopeName</i> parameter.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.

## -remarks

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.