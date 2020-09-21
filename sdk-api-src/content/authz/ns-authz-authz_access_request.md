---
UID: NS:authz._AUTHZ_ACCESS_REQUEST
title: AUTHZ_ACCESS_REQUEST (authz.h)
description: Defines an access check request.
helpviewer_keywords: ["*PAUTHZ_ACCESS_REQUEST","AUTHZ_ACCESS_REQUEST","AUTHZ_ACCESS_REQUEST structure [Security]","PAUTHZ_ACCESS_REQUEST","PAUTHZ_ACCESS_REQUEST structure pointer [Security]","_win32_authz_access_request","authz/AUTHZ_ACCESS_REQUEST","authz/PAUTHZ_ACCESS_REQUEST","security.authz_access_request"]
old-location: security\authz_access_request.htm
tech.root: security
ms.assetid: 3748075c-b31a-4669-b8a6-1a540449d8fa
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_ACCESS_REQUEST, AUTHZ_ACCESS_REQUEST, AUTHZ_ACCESS_REQUEST structure [Security], PAUTHZ_ACCESS_REQUEST, PAUTHZ_ACCESS_REQUEST structure pointer [Security], _win32_authz_access_request, authz/AUTHZ_ACCESS_REQUEST, authz/PAUTHZ_ACCESS_REQUEST, security.authz_access_request'
req.header: authz.h
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
req.typenames: AUTHZ_ACCESS_REQUEST, *PAUTHZ_ACCESS_REQUEST
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_ACCESS_REQUEST
 - authz/_AUTHZ_ACCESS_REQUEST
 - PAUTHZ_ACCESS_REQUEST
 - authz/PAUTHZ_ACCESS_REQUEST
 - AUTHZ_ACCESS_REQUEST
 - authz/AUTHZ_ACCESS_REQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_ACCESS_REQUEST
---

# AUTHZ_ACCESS_REQUEST structure


## -description

The <b>AUTHZ_ACCESS_REQUEST</b> structure defines an access check request.

## -struct-fields

### -field DesiredAccess

The type of access to test for.

### -field PrincipalSelfSid

The <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) to use for the principal self SID in the <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

### -field ObjectTypeList

An array of <a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a> structures in the object tree for the object. Set to <b>NULL</b> unless the application checks access at the property level.

### -field ObjectTypeListLength

The number of elements in the <i>ObjectTypeList</i> array. This member is necessary only if the application checks access at the property level.

### -field OptionalArguments

A pointer to memory to pass to <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> when checking callback <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs).

## -see-also

<a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a>