---
UID: NS:authz._AUTHZ_ACCESS_REQUEST
title: AUTHZ_ACCESS_REQUEST (authz.h)
author: windows-sdk-content
description: Defines an access check request.
old-location: security\authz_access_request.htm
tech.root: SecAuthZ
ms.assetid: 3748075c-b31a-4669-b8a6-1a540449d8fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PAUTHZ_ACCESS_REQUEST, AUTHZ_ACCESS_REQUEST, AUTHZ_ACCESS_REQUEST structure [Security], PAUTHZ_ACCESS_REQUEST, PAUTHZ_ACCESS_REQUEST structure pointer [Security], _win32_authz_access_request, authz/AUTHZ_ACCESS_REQUEST, authz/PAUTHZ_ACCESS_REQUEST, security.authz_access_request"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_ACCESS_REQUEST
product: Windows
targetos: Windows
req.typenames: AUTHZ_ACCESS_REQUEST, *PAUTHZ_ACCESS_REQUEST
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# AUTHZ_ACCESS_REQUEST structure


## -description


The <b>AUTHZ_ACCESS_REQUEST</b> structure defines an access check request.


## -struct-fields




### -field DesiredAccess

The type of access to test for.


### -field PrincipalSelfSid

The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to use for the principal self SID in the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


### -field ObjectTypeList

An array of <a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a> structures in the object tree for the object. Set to <b>NULL</b> unless the application checks access at the property level.


### -field ObjectTypeListLength

The number of elements in the <i>ObjectTypeList</i> array. This member is necessary only if the application checks access at the property level.


### -field OptionalArguments

A pointer to memory to pass to <a href="https://msdn.microsoft.com/e8a510e6-0739-4765-ad07-3bcb1b9c905c">AuthzAccessCheckCallback</a> when checking callback <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs).


## -see-also




<a href="https://msdn.microsoft.com/e8a510e6-0739-4765-ad07-3bcb1b9c905c">AuthzAccessCheckCallback</a>
 

 

